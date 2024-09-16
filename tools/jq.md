
find number of properties with value of false

payload: 
```
{
"test1":false,
"test2":false,
"test3":true,
"test4":false
}
```
query:
```jq -r '.jsonPayload | [. | to_entries | .[] | select(.value==false)]| length' ```

ouput: 
```
3
```
