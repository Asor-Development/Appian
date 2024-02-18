# 
- **Innodb engine settings:**
            - maria db default store engine is Innodb
            - there are different store engines such as ARIAL, MEMORYM TOKUDB, MYISAM etc... there are as many as 10 engines
            - **Buffer Pool size:**
                - Performace Tuning Parameters:
                    -  `innodb_buffer_pool`: it is a standard to allocate 70% of RAM, so if you have 8GB of RAM allocate 5000 MB(Memory Capping)
            - **Page size:**