# sqlw

Example:

```go
package main

import (
    _ "github.com/go-sql-driver/mysql"
    "github.com/pamayung/sqlw"
    "log"
)
func main() {
    masterDSN := "user:password@tcp(master_ip:master_port)/database_name"
    slave1DSN := "user:password@tcp(slave_ip:slave_port)/database_name"
    dsn := masterDSN + ";" + slave1DSN
    
    db, err = sqlt.Open("mysql", dsn)
    if err != nil {
      log.Println("Error ", err.Error())
    }
}
