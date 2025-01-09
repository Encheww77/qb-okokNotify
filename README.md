![image](https://github.com/user-attachments/assets/e221d21e-0d5f-437e-9466-beb1a6f8618d)

.1 Step - Go to [qb]/qb-core/client/function.lua


.2 Step - Look for "QBCore.Functions.Notify" that is around line 153 and 

.3 Step - and replace the code with this snipet 

```
QBCore.Functions.Notify = function(Message, Type, Time, Title)
   local Title = Title ~= nil and Title or "Notification"
   local Message = Message ~= nil and Message or "Message"
   local Time = Time ~= nil and Time or 2000
   local Type = Type ~= nil and Type or "info"
   if ttype == 'primary' then ttype = 'info' end
   exports['okokNotify']:Alert(Title, Message, Time, Type)
end
