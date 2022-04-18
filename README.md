jq snippets
===========


### Description
`jq` recipies and snippets.


### Recipe 01: Has field, field populated and field contains value
```
.[] 
| select(has("Description") and .Description and (.Description | contains("8166-01536")))
```

### Recipe 02: Output to CSV file
```
.[] 
|[.id, .name, .public_name, .space_amount, .collaboration_start_date, .login, .email, .enterprise_id ] 
| @csv

```