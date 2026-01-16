# 🚀 Quick Start Guide

## Passo 1: Criar Conta no Redis Cloud

1. Acesse https://redis.com/try-free/
2. Crie uma conta gratuita
3. Após login, clique em "Create database"
4. Selecione o plano **Free** (30MB)
5. Escolha a região mais próxima (ex: AWS us-east-1)
6. Clique em "Activate"

## Passo 2: Obter Credenciais

Após criar o database:

1. Clique no database criado
2. Na aba "Configuration", você verá:
   - **Endpoint** (ex: `redis-12345.c123.us-east-1-1.ec2.cloud.redislabs.com:12345`)
   - **Default user password** (clique no ícone do olho para revelar)

3. Anote estas informações:
   ```
   Host: redis-12345.c123.us-east-1-1.ec2.cloud.redislabs.com
   Port: 12345
   Password: sua-senha-aqui
   ```

## Passo 3: Instalar Dependências

No terminal, execute:

```bash
pip install -r requirements.txt
```

## Passo 4: Iniciar o Notebook

```bash
jupyter notebook
```

Isso abrirá o navegador automaticamente.

## Passo 5: Configurar Conexão

1. Abra o arquivo `redis_workshop.ipynb`
2. Na segunda célula de código, substitua:

```python
REDIS_HOST = "redis-12345.c123.us-east-1-1.ec2.cloud.redislabs.com"
REDIS_PORT = 12345
REDIS_PASSWORD = "sua-senha-aqui"
```

3. Execute a célula (Shift + Enter)
4. Você deve ver: ✅ Conexão com Redis estabelecida com sucesso!

## Passo 6: Começar o Workshop

Execute as células sequencialmente usando **Shift + Enter** ou clicando no botão "Run".

## 🆘 Problemas Comuns

### Erro de Conexão

```
❌ Erro ao conectar: Error connecting to Redis
```

**Solução:**
- Verifique se o host, port e password estão corretos
- Verifique se seu firewall permite conexões na porta especificada
- Teste a conexão usando Redis Insight

### Módulo não encontrado

```
ModuleNotFoundError: No module named 'redis'
```

**Solução:**
```bash
pip install redis
```

### RedisJSON ou RedisBloom não disponível

```
ResponseError: unknown command 'JSON.SET'
```

**Solução:**
- Isso é normal! O notebook tem alternativas usando strings
- Para habilitar RedisJSON/RedisBloom, você precisa de um plano pago ou usar Redis Stack localmente

## 📱 Usando Redis Insight (Opcional)

Redis Insight é uma ferramenta gráfica para visualizar seus dados:

1. Download: https://redis.io/insight/
2. Instale e abra o aplicativo
3. Clique em "Add Database"
4. Escolha "Connect to a Redis Database"
5. Insira suas credenciais
6. Explore visualmente os dados criados pelo notebook!

## ✅ Pronto!

Agora você está pronto para começar o workshop. Divirta-se aprendendo Redis! 🎉

