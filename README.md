# **PERN Template (*ts_prisma_vite*)**

<pre>
  <strong>Updated</strong>
     Code:   7/9/2023
</pre>

**Contents**  
>**[1. Overview](#1-overview)**  
**[2. Getting Started](#2-getting-started)**  
**[3. Notes](#3-notes)**  

### 1. Overview  
> **Includes**:  
> • Typescript  
> • Prisma (ORM)  
> • VITE (Front End Tooling) - added react-router-dom  
> **Requires**:  
> • Linux or WSL for Windows (v2 recommended)  
> • Docker  
> • Official Postgres Docker Image  
> • Node  

### 2. Getting Started
>  #### Step 1 - Start Docker Container w/ Postgres
  >  1. open terminal (starts database instance in docker)  
  > <sup>Note: Windows Users must be using WSL </sup>
  >   * `cd database` 
  >   * `./run-postgres.sh`  
  >
  > 2. open new terminal (not required, this is a manual check that docker container is running and psql is valid)  
  >   * `docker exec -it postgres-dev bash` 
  >   * `psql -h localhost -p 5432 -U postgres`  
  >   * Enter password for user postgres, default: **`password`**
  >     * <sup> `\l` for list of databases  
  >                   `\c devdb` to connect to a database  
  >                   `\dt` to show tables  
  >                   `\d` to show tables, views, and sequences 
  > 
  >
>  #### Step 2 - Start Server
  >  1. open terminal (seeds database?)  
  > <sup>Note: Windows Users must be using WSL </sup>  
  >   * `cd server` 
  >   * `npx prisma migrate dev --name init`  
  >  
  > 2. open new terminal (watches and compiles typescript)  
  >   * `cd server` 
  >   * `npm run dev:tsc`  
  >  
  > 2. open new terminal (watches and runs javascript)  
  >   * `cd server` 
  >   * `npm run dev:server`  
  > 
  >
>  #### Step 3 - Start App
  >  1. open terminal (starts front-end)  
  > <sup>Note: Windows Users must be using WSL </sup>  
  >   * `cd app/pern-blueprint` 
  >   * `npm install` 
  >   * `npm run dev`  
  >  
  >  


### 3. Notes
> Node 18 was used
> WSL v2 for Windows was used
---
<sup>Used https://stackedit.io/app# to format this README