# immich

## Parameters

### Common parameters

| Name           | Description                                        | Type       | Value  |
| -------------- | -------------------------------------------------- | ---------- | ------ |
| `host`         | Hostname for external access.                      | `string`   | `""`   |
| `size`         | Persistent Volume Claim size for application data. | `quantity` | `10Gi` |
| `storageClass` | StorageClass used to store the data.               | `string`   | `""`   |


### Database configuration

| Name                | Description                                                                                         | Type       | Value    |
| ------------------- | --------------------------------------------------------------------------------------------------- | ---------- | -------- |
| `database`          | PostgreSQL configuration.                                                                           | `object`   | `{}`     |
| `database.size`     | Persistent Volume size for database storage.                                                        | `quantity` | `10Gi`   |
| `database.replicas` | Number of database instances.                                                                       | `int`      | `2`      |
| `database.user`     | Database user to create.                                                                            | `string`   | `immich` |
| `database.name`     | Database name to create.                                                                            | `string`   | `immich` |
| `database.password` | Optional password. When empty, the cozystack postgres chart generates and preserves one via lookup. | `string`   | `""`     |


### Redis configuration

| Name             | Description                               | Type       | Value |
| ---------------- | ----------------------------------------- | ---------- | ----- |
| `redis`          | Redis configuration.                      | `object`   | `{}`  |
| `redis.size`     | Persistent Volume size for redis storage. | `quantity` | `1Gi` |
| `redis.replicas` | Number of redis replicas.                 | `int`      | `2`   |

