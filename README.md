# Go API - Gerador de boilerplate
### Install
go install github.com/discord-gophers/goapi-gen@latest
### Generator
goapi-gen --out ./internal/api/spec/journey.gen.spec.go ./internal/api/spec/journey.spec.json

### Go
go mod init journey  <!-- iniciar módulo em go -->
go mod tidy          <!-- install dep -->
go get -u ./...      <!-- update dep -->
go generate ./...

### Sqlc
go install github.com/sqlc-dev/sqlc/cmd/sqlc@latest

### Tern
go install github.com/jackc/tern/v2@latest
tern init ./internal/pgstore/migrations
<!-- pode apagar o arquivo de exemplo em migrations -->
<!-- limpar o arquivo tern.conf -->

tern new --migrations ./internal/pgstore/migrations create_trips_table
tern new --migrations ./internal/pgstore/migrations create_participants_table
tern new --migrations ./internal/pgstore/migrations create_activities_table
tern new --migrations ./internal/pgstore/migrations create_links_table

tern migrate --migrations ./internal/pgstore/migrations --config ./internal/pgstore/migrations/tern.conf

### ENV
inserir variáveis no .zshrc
source ~/.zshrc

### Links
https://github.com/rocketseat-education/nlw-journey-go/
https://nlw-journey.apidocumentation.com/reference
https://editor.swagger.io/
https://github.com/discord-gophers/goapi-gen
https://github.com/sqlc-dev/sqlc
https://github.com/doug-martin/goqu
https://github.com/Masterminds/squirrel
https://github.com/jackc/pgx <!-- Postgresql com go -->
https://github.com/google/uuid
https://github.com/tern-tools/tern <!-- Cria migrations em go -->
https://github.com/go-playground/validator
https://github.com/wneessen/go-mail
https://pkg.go.dev/html/template