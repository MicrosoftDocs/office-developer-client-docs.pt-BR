---
title: Em massa de campos personalizados de atualização e criar sites de projetos no Project Online
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 815131c6-190c-4f29-83bf-c853eee72821
description: Para ajudar os clientes a aproveitar ao máximo Project Online e melhorar nossos extensibilidade de serviço e a flexibilidade, adicionamos dois métodos para o modelo de objeto do cliente que podem ser usados nos fluxos de trabalho e aplicativos do Project Online.
ms.openlocfilehash: 4f8fee5de5efb69f410b78e9ce93b9dc9bb133f3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771057"
---
# <a name="bulk-update-custom-fields-and-create-project-sites-from-a-workflow-in-project-online"></a>Atualizar campos personalizados em massa e criar sites de projeto a partir de um fluxo de trabalho no Project Online

Para ajudar os clientes a aproveitar ao máximo Project Online e melhorar nossos extensibilidade de serviço e a flexibilidade, adicionamos dois métodos para o modelo de objeto do cliente que podem ser usados nos fluxos de trabalho e aplicativos do Project Online.
  
|||
|:-----|:-----|
|**UpdateCustomFields** <br/> |Em massa atualiza os campos personalizados do projeto. Para o Project Online somente. Disponível somente na API REST.  <br/> |
|**CreateProjectSite** <br/> | Cria um site de projeto. Para o Project Online somente. Disponível na API REST, modelo de objeto do cliente gerenciado e modelo de objeto de cliente JavaScript.  <br/> |
   
Além de fornecer mais flexibilidade, esses métodos também oferecem significativos aprimoramentos de desempenho quando salvar e publicar projetos em um fluxo de trabalho. Este artigo descreve como usar os métodos na API REST e fornece instruções para criar um fluxo de trabalho que campos personalizados de atualizações em massa e um fluxo de trabalho que cria um site de projeto.
  
> [!NOTE]
> Para saber mais sobre chamando APIs REST a partir de fluxos de trabalho do SharePoint 2013, consulte [REST do SharePoint usando os serviços de fluxo de trabalho com o método POST](http://mysharepointinsight.blogspot.com/2013/05/using-sharepoint-rest-services-from.mdl) e [chamando a API do SharePoint 2013 Rest a partir de um fluxo de trabalho do SharePoint Designer](https://sergeluca.wordpress.com/2013/04/09/calling-the-sharepoint-2013-rest-api-from-a-sharepoint-designer-workflow/). 
  
## <a name="bulk-update-project-custom-fields-from-a-workflow"></a>Atualização em massa campos personalizados do projeto a partir de um fluxo de trabalho
<a name="BulkUpdateCustomFields"> </a>

Anteriormente, fluxos de trabalho só podem atualizar um campo personalizado por vez. Atualizar os campos personalizados do projeto um por vez pode resultar em uma experiência de usuário final ruim quando os usuários fazer a transição entre páginas de detalhes do projeto. Cada atualização necessária uma solicitação de um servidor separado usando a ação **Definir campo de projeto** e atualizar vários campos personalizados em uma latência alta, baixa largura de banda rede resultou em uma sobrecarga não rotineira. Para resolver esse problema, adicionamos o método **UpdateCustomFields** para a API REST que permite a que você em massa atualizar campos personalizados. Para usar **UpdateCustomFields**, você passar um dicionário que contém os nomes e valores de todos os campos personalizados que você deseja atualizar.
  
O método REST pode ser encontrado no ponto de extremidade seguir:
  
`https://<site-url>/_api/ProjectServer/Projects('<guid>')/Draft/UpdateCustomFields()`
  
> [!NOTE]
> Substituir o `<site-url>` espaço reservado nos exemplos com a URL do seu site do Project Web App (PWA) e o `<guid>` espaço reservado com seu projeto UID. 
  
Esta seção descreve como criar um fluxo de trabalho em massa atualizações de campos personalizados de um projeto. O fluxo de trabalho segue estas etapas de alto nível:
  
- Aguarde o projeto que você deseja atualizar para fazer check-in
    
- Criar um conjunto de dados que define todas as suas atualizações de campo personalizado para o projeto
    
- Fazer check-out do projeto
    
- Chamar **UpdateCustomFields** para aplicar as atualizações de campo personalizado ao projeto 
    
- Faça logon informações relevantes para a lista de histórico do fluxo de trabalho (se necessário)
    
- Publicar o projeto
    
- Fazer check-in do projeto
    
O fluxo de trabalho de ponta a ponta, final tem esta aparência:
  
![Fluxo de trabalho de ponta a ponta] (media/8c0741f9-7f76-409d-8c00-e7a8c3ddb89f.png "Fluxo de trabalho de ponta a ponta")
  
### <a name="to-create-a-workflow-that-bulk-updates-custom-fields"></a>Para criar um fluxo de trabalho em massa atualizações de campos personalizados

1. Opcional. Armazene a URL completa do seu projeto em uma variável que você pode usar em todo o fluxo de trabalho.
    
    ![A URL do projeto em uma variável de repositório] (media/a880c5c6-8e7a-44dd-87e9-7e532169d489.png "A URL do projeto em uma variável de repositório")
  
2. Adicione a ação de **aguardar o evento de projeto** ao fluxo de trabalho e escolha o evento **quando um projeto check-in** . 
    
    ![Aguarde o projeto a ser verificado] (media/699aa9c7-b3c9-426e-a775-96993a13559c.png "Aguarde o projeto a ser verificado")
  
3. Crie um dicionário de **requestHeader** usando a ação de **compilação de dicionário** . Você usará o mesmo cabeçalho de solicitação para todas as chamadas de serviço da web neste fluxo de trabalho. 
    
    ![Crie o dicionário requestHeader] (media/83b0aa10-9ab7-43dd-800d-a738bb815876.png "Crie o dicionário requestHeader")
  
4. Adicione os seguintes itens ao dicionário.
    
    |Name|Tipo|Value|
    |:-----|:-----|:-----|
    |Accept  <br/> |String  <br/> |aplicativo/json; OData = verbose  <br/> |
    |Content-Type  <br/> |String  <br/> |aplicativo/json; OData = verbose  <br/> |
   
    ![Adicionando um cabeçalho Accept] (media/2f2e2016-3c49-4cac-b1e7-f2b8118b840c.png "Adicionando um cabeçalho Accept")
  
5. Crie um dicionário de **requestBody** usando a ação de **compilação de dicionário** . Esse dicionário armazena todas as atualizações do campo que você deseja aplicar. 
    
    Cada atualização de campo personalizado requer quatro linhas: tipo (1) de metadados, (2) a chave, (3) valor e tipo (4) o valor do campo.
    
    - **__metadata/tipo** Tipo de metadados do campo. Esse registro é sempre o mesmo e usa os seguintes valores: 
    
       - Nome: customFieldDictionary (i) / __metadata/tipo (onde **i** é o índice de cada campo personalizado no dicionário, começando com 0) 
            
       - Tipo: String
            
       - Valor: SP. KeyValue
    
       ![Definindo uma atualização de campo personalizado] (media/a4423493-6603-42ee-ae50-1ef74c5c59bd.png "Definindo uma atualização de campo personalizado")
  
    - **Chave** O nome interno do campo personalizado, no formato: *Custom_ce23fbf43fa0e411941000155d3c8201* 
    
       Você pode encontrar o nome interno de um campo personalizado navegando até a extremidade do **InternalName** :`https://<site-url>/_api/ProjectServer/CustomFields('<guid>')/InternalName`
    
       Se você criou seus campos personalizados manualmente, os valores serão diferentes de um site para outro. Se você pretende reutilizar o fluxo de trabalho em vários sites, verifique se o campo personalizado IDs estão corretas.
    
    - **Valor** O valor a ser atribuído ao campo personalizado. Para campos personalizados que são vinculados a tabelas de pesquisa, você precisa usar os nomes de internos das entradas de tabela de pesquisa, em vez de valores de tabela de pesquisa real. 
    
       Você pode encontrar o nome interno da entrada da tabela de pesquisa no ponto de extremidade seguir:`https://<site-url>/_api/ProjectServer/CustomFields('<guid>')/LookupEntries('<guid>')/InternalName`
    
       Se você tiver um campo personalizado da tabela de pesquisa configurado para aceitar vários valores, use `;#` concatenar valores (conforme mostrado no dicionário exemplo abaixo). 
    
    - **ValueType** O tipo de campo personalizado que você está atualizando. 
    
       - Para campos de texto, duração, sinalizador e LookupTable, use Edm.String
    
       - Para campos numéricos, use Edm.Int32, Edm.Double ou qualquer outro aceitos OData número tipo
    
       - Para campos de data, use Edm.DateTime
    
       O dicionário de exemplo abaixo define atualizações para três campos personalizados. A primeira é de um campo personalizado vários do valor pesquisa tabela, o segundo é para um campo de número e a terceira é destinada um campo date. Observação como incrementos de índice do **customFieldDictionary** . 
    
       > [!NOTE]
       > Esses valores são apenas para fins ilustrativos. Os pares de chave-valor que você utilizará dependem de seus dados do PWA. 
  
       |Name|Tipo|Value|
       |:-----|:-----|:-----|
       |tipo/__metadata/customFieldDictionary (0)  <br/> |String  <br/> |SP. KeyValue  <br/> |
       |customFieldDictionary (0) tecla /  <br/> |String  <br/> |Sinalizador\_ce23fbf43fa0e411941000155d3c8201  <br/> |
       |customFieldDictionary (0) / valor  <br/> |String  <br/> |Entrada\_b9a2fd69279de411940f00155d3c8201; #Entry\_baa2fd69279de411940f00155d3c8201  <br/> |
       |customFieldDictionary (0) / ValueType  <br/> |String  <br/> |Edm.String  <br/> |
       |customFieldDictionary (1) / __metadata/tipo  <br/> |String  <br/> |SP. KeyValue  <br/> |
       |customFieldDictionary (1) / chave  <br/> |String  <br/> |Custom_c7f114c97098e411940f00155d3c8201  <br/> |
       |customFieldDictionary (1) / valor  <br/> |String  <br/> |90.5  <br/> |
       |customFieldDictionary (1) / ValueType  <br/> |String  <br/> |Edm.Double  <br/> |
       |customFieldDictionary (2) / __metadata/tipo  <br/> |String  <br/> |SP. KeyValue  <br/> |
       |customFieldDictionary (2) / chave  <br/> |String  <br/> |Custom_c6fb67e0b9a1e411941000155d3c8201  <br/> |
       |customFieldDictionary (2) / valor  <br/> |String  <br/> |2015-04-01T00:00:00.0000000  <br/> |
       |customFieldDictionary (2) / ValueType  <br/> |String  <br/> |Edm.DateTime  <br/> |
   
       ![Dicionário que define as atualizações de campo personalizado] (media/41a1f18f-a6b2-40ff-904b-437baf962621.png "Dicionário que define as atualizações de campo personalizado")
  
6. Adicione uma ação de **Chamada serviço da Web de HTTP** para Confira o projeto. 
    
    ![Chame o método de check-out] (media/8ce56014-0317-419b-afa7-229d05c86885.png "Chame o método de check-out")
  
7. Edite as propriedades da chamada de serviço web para especificar o cabeçalho de solicitação. Para abrir a caixa de diálogo **Propriedades** , a ação do mouse em e escolha **Propriedades**.
    
    ![Especificar o cabeçalho de solicitação no serviço web propriedades da chamada] (media/d81e92b1-43df-42ad-9cd0-a693f93b164e.png "Especificar o cabeçalho de solicitação no serviço web propriedades da chamada")
  
8. Adicione uma ação de **Chamada serviço da Web de HTTP** para chamar o método **UpdateCustomFields** . 
    
    ![Criar uma ação de chamada serviço da Web de HTTP] (media/9a73a201-c035-41b4-8798-506ac48b90f8.png "Criar uma ação de chamada serviço da Web de HTTP")
  
    Observação o `/Draft/` segmento na URL do serviço web. A URL completa deve ter esta aparência:`https://<site-url>/_api/ProjectServer/Projects('<guid>')/Draft/UpdateCustomFields()`
    
    ![Chame o método UpdateCustomFields] (media/03b323f1-8e99-4b18-be18-be505d7cec7e.png "Chame o método UpdateCustomFields")
  
9. Edite as propriedades da chamada de serviço web para vincular os parâmetros **RequestHeader** e **RequestContent** aos dicionários que você criou. Você também pode criar uma nova variável para armazenar o **ResponseContent**.
    
    ![Associe os dicionários ao cabeçalho da solicitação e conteúdo] (media/f96bec92-138e-4eab-b1e7-1ab83d0428a5.png "Associe os dicionários ao cabeçalho da solicitação e conteúdo")
  
10. Opcional. Ler o dicionário de resposta para verificar o estado do trabalho em fila e registrar as informações na lista de histórico do fluxo de trabalho.
    
    ![Configurações de log] (media/7d2f4936-61d7-4906-83e8-7478a5935af5.png "Configurações de log")
  
11. Adicione uma chamada de serviço web para o ponto de extremidade de **Publicar** para publicar o projeto. Sempre use o mesmo cabeçalho de solicitação. 
    
    ![Chamar o método Publish] (media/3b661091-ffae-4d7e-a0bb-5b96a6292731.png "Chamar o método Publish")
  
    ![Propriedades do serviço web Publish chamada] (media/6a80a5d3-7e29-4398-993c-f78b3faca8b1.png "Propriedades do serviço web Publish chamada")
  
12. Adicione uma chamada ao serviço web final ao ponto de extremidade **Checkin** fazer check-in do projeto. 
    
    ![Chame o método Checkin] (media/430510cb-0774-4911-af7f-b565b83eba0e.png "Chame o método Checkin")
  
    ![Chamada de propriedades para o serviço web de check-in] (media/485f48d6-bbb8-4568-9dc3-aae3218f6bd1.png "Chamada de propriedades para o serviço web de check-in")

<a name="CreateProjectSite"> </a>

## <a name="create-a-project-site-from-a-workflow"></a>Criar um site de projeto a partir de um fluxo de trabalho

Cada projeto pode ter seus próprio sites dedicados do SharePoint onde os membros da equipe podem colaborar, compartilhar documentos, eleve problemas e assim por diante. Anteriormente, sites só podiam ser criadas automaticamente nas primeiro publique ou manualmente pelo gerente de projeto no Project Professional ou pelo administrador no PWA configurações ou eles poderiam ser desabilitado.
  
Adicionamos o método **CreateProjectSite** para que você possa escolher quando criar sites de projetos. Isso é particularmente útil para organizações que deseja criar seus sites automaticamente quando uma proposta de projeto atinge um estágio específico em um fluxo de trabalho predefinido, em vez de na primeira publicar. Adiar a criação de site de projeto significativamente melhora o desempenho de criação de um projeto. 
  
**Pré-requisito:** Antes de poder usar **CreateProjectSite**, a configuração **Permitir que os usuários escolham** deve ser definida para a criação de site de projeto no **PWA configurações** > * * Sites do SharePoint conectados * * > **configurações**.
  
![Configuração "Permitir que os usuários escolham" nas configurações do PWA] (media/6c6c8175-eb10-431d-8056-cea55718fdb4.png "Configuração Permitir que usuários escolher nas configurações do PWA")
  
### <a name="to-create-a-workflow-that-creates-a-project-site"></a>Para criar um fluxo de trabalho que cria um site de projeto

1. Criar ou editar um fluxo de trabalho existente e selecione a etapa onde você deseja criar seus sites de projeto.
    
2. Crie um dicionário de **requestHeader** usando a ação de **compilação de dicionário** . 
    
    ![Crie o dicionário requestHeader] (media/83b0aa10-9ab7-43dd-800d-a738bb815876.png "Crie o dicionário requestHeader")
  
3. Adicione os seguintes itens ao dicionário.
    
    |Name|Tipo|Value|
    |:-----|:-----|:-----|
    |Accept  <br/> |String  <br/> |aplicativo/json; OData = verbose  <br/> |
    |Content-Type  <br/> |String  <br/> |aplicativo/json; OData = verbose  <br/> |
   
    ![Adicionando um cabeçalho Accept] (media/2f2e2016-3c49-4cac-b1e7-f2b8118b840c.png "Adicionando um cabeçalho Accept")
  
4. Adicione a ação de **Chamada serviço da Web de HTTP** . Altere o tipo de solicitação para usar o **POST**e definir a URL usando o seguinte formato:
    
    `https://<site-url>/_api/ProjectServer/Projects('<guid>')/CreateProjectSite('New web name')`
    
    ![Construir o URI do ponto de extremidade de CreateProjectSite] (media/42a90a5e-8d1b-4667-a933-785175212847.png "Construir o URI do ponto de extremidade de CreateProjectSite")
  
    Passe o nome do site de projeto para o método **CreateProjectSite** como uma cadeia de caracteres. Para usar o nome do projeto como o nome do site, passe uma sequência vazia. Certifique-se de usar nomes exclusivos para que o próximo site de projeto que você criar funcione. 
    
5. Edite as propriedades da chamada de serviço web para vincular o parâmetro **RequestHeader** ao dicionário que você criou. 
    
    ![Associando o dicionário à solicitação] (media/61a5a0a8-405f-44eb-b5e7-80b11f7caec3.png "Associando o dicionário à solicitação")
  
## <a name="see-also"></a>Confira também

- [Tarefas de programação do Project](project-programming-tasks.md)
- [Modelo de objeto do cliente (CSOM) para o Project 2013](client-side-object-model-csom-for-project-2013.md)
- [Fluxos de trabalho no SharePoint 2013](http://msdn.microsoft.com/library/e0602371-ae22-44be-8a7e-9e47e9f046d6%28Office.15%29.aspx)
    

