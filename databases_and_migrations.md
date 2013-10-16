# MySQL

```sql
show index in my_table;
drop index dn_ownerships_ix on my_table;

```

# PostgreSQL

# Rails migrations

### Add and remove index

```ruby
class AddDocumentNameOwnershipIndex < ActiveRecord::Migration
  def up
    add_index :document_name_ownerships, 
      [:owner_type, :owner_id],
      name: :dn_ownerships_ix
  end

  def down
    remove_index :document_name_ownerships, name: :dn_ownerships_ix
  end
end
```