## Setup DB

```bash
PGPASSWORD='postgres'
createdb -U postgres -h db seshalab
pg_restore -d seshalab -U postgres -h db -p 5432 SeshaLab-PostgreSql.backup
```
```bash
psql -U postgres -h db -p 5432 -c "DROP DATABASE seshalab;"
```

## Retore dependencies

```bash
cd adminportal
pnpm install
```

```bash
cd publicportal
pnpm install
```

```bash
cd backend
dotnet restore
```

## Start

```bash
cd adminportal
pnpm start dev
```

```bash
dotnet run --project src/EP.SeshaLab.Web.Host/EP.SeshaLab.Web.Host.csproj --launch-profile Project
```