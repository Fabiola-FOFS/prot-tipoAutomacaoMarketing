foram criados 2 fluxos
a ideia inicial era criar no N8N um webhook, um nó condicional que disparia e-mails automaticos de forma segmentada de acordo com o resultado do simulado. Isto porque no plano gratuíto do RD não é possivel criar uma segmentação, enviar e-mails diferentes para perfis diferentes. 
Mas tive problemas para configurar um gmail que pudesse ser usado para disparo em massa. Tive que repensar, e mudei a ideia para usar o N8N apenas para captar os dados e salvar em um documento. Já que não pude conectar o google analitics no RD devido as limitações do periodo de teste. 

print 1 fluxo 1: enviando e-mails diferentes para perfis diferentes:

![alt text](../prints/fluxo1N8N.png)

tentei também criar um fluxo para captar e-mail e resultado do simulado e enviar para uma planilha (ainda em testes)
![alt text](<../prints/teste no N8N de captação e segmentação - Falhou.png>)

print 2 fluxo 2 : dados captados vão para planilha (ainda em validaçãoS)

Formulário de confirmação (email)
        ↓
Simulado (resultado.html?perfil=...)
        ↓
Webhook 2 (perfil + email)
        ↓
Google Sheets (salva linha)
![alt text](<../prints/fluxo 2 n8n.png>) 