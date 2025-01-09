![image](https://github.com/user-attachments/assets/e221d21e-0d5f-437e-9466-beb1a6f8618d)

.1 Step - Go to [qb]/qb-core/client/function.lua


.2 Step - Look for "QBCore.Functions.Notify" that is around line 153 and 

.3 Step - and replace the code with this snipet 

```
function QBCore.Functions.Notify(text, textype, length)
    if textype == 'primary' then textype = 'info' end 
    local ttype = textype ~= nil and textype or "info"
    local length = length ~= nil and length or 5000
    exports['okokNotify']:Alert("", text, length, ttype)
end
