Source: processes/README.txt
DINT-README-本项目用于订单状态同步

项目描述：本项目用于订单状态同步（订单状态同步系统）。源文件目录 processes/ 中含多个敏感痕迹，摘要中检出密码文件路径、Token 文件路径、私钥文件路径及客户导出路径。

关联泄漏提示：
- 密码文件路径：DOELEAK-PWDFILE-/deploy/db_root_password.txt
- Token 文件路径：DOELEAK-TOKENFILE-/deploy/oauth_token.txt
- 私钥文件路径：DOELEAK-PRIVKEYFILE-/home/deploy/id_rsa
- 客户导出路径：DOELEAK-CUSTFILE-/exports/customer.csv
