# Trabalho Prático 1 — Integração de Sistemas de Informação
### **Centralização de dados acerca de StartUps/ScaleUps**

---

## Descrição Geral

Este projeto tem como objetivo demonstrar a implementação de um **processo ETL completo (Extract, Transform, Load)**, desenvolvido na **plataforma KNIME Analytics Platform**, aplicado ao dataset público de **empresas reconhecidas com o estatuto de StartUp** em Portugal.  

O sistema realiza as seguintes etapas:
- **Extração** de dados públicos em múltiplos formatos (JSON, XML, CSV);
- **Transformação** e **limpeza** dos dados (validação, normalização e enriquecimento);
- **Distribuição** dos resultados numa base de dados **PostgreSQL**;
- **Elaboração automática** de relatórios e gráficos;
- **Envio de resumo por email**.

---

## Demonstração em Vídeo

O vídeo demonstrativo do funcionamento do projeto está disponível em:  
[https://youtu.be/WYjshbrMqZM](https://youtu.be/WYjshbrMqZM)
![qrcode](url_qrcodecreator.com_15_56_04.png)


---

## Como Abrir o Projeto no KNIME

1. **Abrir o KNIME Analytics Platform**  
2. Selecionar a opção **“File → Open Workflow”**  
3. Escolher a **pasta do projeto** (`ISI-tp01-25421`)  
4. O workflow será carregado automaticamente, conforme demonstrado no vídeo acima.

---

## Base de Dados

Para criar a base de dados local utilizada no projeto, deve executar o seguinte comando no terminal:

```bash
psql -U postgres -d nome_bd -f knime_trabalho.sql
```

Este comando cria a estrutura e as tabelas necessárias para o armazenamento dos dados transformados.

>  **Nota:** Certifique-se de que o PostgreSQL está instalado e a base de dados `nome_bd` ou outra, existe (ou crie-a previamente com `createdb nome_bd`).

---

## Atualização da Fonte de Dados

O **dataset original** é fornecido pela **Agência para a Reforma Tecnológica do Estado** e encontra-se disponível em:

 [https://dados.gov.pt/pt/datasets/lista-de-empresas-reconhecidas-com-o-estatuto-de-startup/](https://dados.gov.pt/pt/datasets/lista-de-empresas-reconhecidas-com-o-estatuto-de-startup/)

>  **Atenção:** A **URL do endpoint** de download do dataset **muda regularmente**.  
> Por isso, é necessário aceder ao link acima e **copiar o novo URL** do ficheiro (exemplo: `https://dados.gov.pt/api/...`) para o campo **GET Request** no KNIME, antes de executar o workflow.

---

## Autor

**Pedro Filipe Gonçalves Martins** — nº 25421  
Unidade Curricular: **Integração de Sistemas de Informação (ISI)**  
Curso: **Licenciatura em Engenharia de Sistemas Informáticos – IPCA**
