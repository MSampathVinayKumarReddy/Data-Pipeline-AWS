# Data-Pipeline-AWS

STEP 1

first creating a CONFIG file which stores :
aws credentials - key, secret_key
dwh properties - cluster_type, num_nodes, node_type, cluster_identifier, 
                  db_name, db_user, db_password, dwh_port, dwh_iam_role 

such that no HARD-CODING is involved.

STEP 2

create iam_role for redshift (to access s3 by redshift)
and add S3 FULL access

STEP 3

create a bucket in s3 and dump all the files inside that bucket
create a redshift and add iam role to it

STEP 4

create all the tables in redshift (manually using SQL queries)
now use COPY command to get all the data from S3 to created tables in redshift

FINAL

Once everything is done

CLOSE the connection
DELETE the redshift cluster
