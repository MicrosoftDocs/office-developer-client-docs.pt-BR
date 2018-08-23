---
title: Acessar campos personalizados da empresa no Project Online
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 25509631-fa14-49d8-b594-cfacf5355c38
description: 'Project Online é um serviço do Office 365 que as empresas podem ampliar para atender às necessidades de negócios. Uma área de extensão é campos personalizados da empresa (ECFs). ECFs são campos de valor digitado que podem ser adicionados a projetos, recursos e tarefas. A tabela a seguir lista ECFs associar projetos, recursos e tarefas e fornece um exemplo de um valor para uma instância do que ECF:'
ms.openlocfilehash: d560b258f2c9873844009cb6bc6e698abec029a6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584601"
---
# <a name="accessing-project-online-enterprise-custom-fields"></a>Acessar campos personalizados da empresa no Project Online

Project Online é um serviço do Office 365 que as empresas podem ampliar para atender às necessidades de negócios. Uma área de extensão é campos personalizados da empresa (ECFs). ECFs são campos de valor digitado que podem ser adicionados a projetos, recursos e tarefas. A tabela a seguir lista ECFs associar projetos, recursos e tarefas e fornece um exemplo de um valor para uma instância do que ECF:
  
|Nome do ECF|Tipo ECF|Association|Valor de exemplo|
|:-----|:-----|:-----|:-----|
|Justificativa  <br/> |TEXT  <br/> |Project  <br/> |Um usuário final pode registrar estatísticas importantes e dados de integridade, com os resultados que incluem uma avaliação de integridade e uma ação individualizada plano rumo melhor integridade.  <br/> |
|Classificação de risco  <br/> |TEXT  <br/> |Project  <br/> |Baixa  <br/> |
|RETORNO DO INVESTIMENTO  <br/> |NÚMERO  <br/> |Project  <br/> |2,10  <br/> |
|Custo total  <br/> |CUSTO  <br/> |Project  <br/> |US $1,031,514  <br/> |
|Início da equipe  <br/> |TEXT  <br/> |Resources  <br/> |Sim  <br/> |
|Função posição  <br/> |TEXT  <br/> |Resources  <br/> |Testador  <br/> |
|Status do Sinalizador  <br/> |SINALIZADOR  <br/> |Task  <br/> |Não  <br/> |
|Saúde  <br/> |TEXT  <br/> |Task  <br/> |Não especificado  <br/> |
   
ECFs são definidas na instância do Project Web Application (PWA), externa de qualquer projeto, recurso ou tarefa. Ainda assim, eles podem se tornar associados a um projeto, recurso ou tarefa. Este artigo fornece um olhar introdutório sobre campos personalizados usando um aplicativo de amostra e se concentra em recuperando valores de ECF. 
  
Você pode baixar o exemplo completo em https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields.
  
Além disso, Project Online suporta campos personalizados locais como somente leitura entidades específicas para o projeto específico, recurso ou tarefa. Para obter mais informações sobre campos personalizados locais, consulte o exemplo https://github.com/OfficeDev/Project-CSOM-Read-Local-CustomFields\.
  
## <a name="background-materials"></a>Materiais de plano de fundo

Um artigo anterior, [desenvolvimento de um aplicativo do Project Online usando o modelo de objeto do cliente](developing-a-project-online-application-using-the-client-side-object-model.md), fornece um plano de fundo e a orientação inicial para desenvolver aplicativos usando o CSOM. Consulte este artigo para os seguintes itens:
  
- Informações básicas sobre o projeto, edições autônomos e baseado em nuvem 
    
- Ambiente de desenvolvimento (edições do Visual Studio e bibliotecas de software)
    
- Instalação de projeto do Visual Studio para um aplicativo .NET usando a biblioteca de CSOM
    
- Conectando ao serviço Project Online
    
## <a name="preliminaries-class-level-declarations"></a>Etapas preliminares (nível da classe declarations)

A classe para esse aplicativo define dois itens de dados: o contexto de projeto e o dicionário de pwaECF.
  
O objeto de contexto do projeto é parte do CSOM do projeto e conecta-se o aplicativo e a instância do PWA. Todas as solicitações ao serviço usam o contexto do projeto.
  
```cs
private static ProjectContext projContext = 
     new ProjectContext("https://Contoso216.sharepoint.com/sites/pwa");

```

O contexto precisa o ponto de extremidade de conexão para criar uma instância de um aplicativo. O ponto de extremidade de conexão é a URL da sua instância do PWA. 
  
O dicionário pwaECF armazena o projeto ECFs definidas no nível do PWA. O dicionário usa o ECF. InternalName como a chave e o objeto CustomField como o valor. O dicionário é preenchido no método ListPWACustomFields e, em seguida, usado como uma referência no método Main. 
  
```cs
    //Dictionary of ECFs
        static Dictionary<String, CustomField> pwaECF = new Dictionary<string, CustomField>();

```

## <a name="main-method"></a>Método principal

O método Main gerencia o fluxo de aplicativo. Como com outros aplicativos que usam o Project Online CSOM Main inicializa o contexto do projeto. 
  
1. Recupere e listar os ECFs no Project Online PWA.
    
   Essa funcionalidade é implementada no método ListPWACustomFields.
    
2. Recupere os projetos com campos personalizados e não personalizadas.
    
   Ao recuperar projetos com ECFs, a solicitação de consulta para o serviço do Project Online precisa incluir os seguintes itens: 
    
   - **IncludeCustomFields** &ndash; Esse item solicita o serviço para retornar uma coleção de PublishedProjects onde cada projeto publicado inclui uma extensão que ofereça suporte a campos personalizados. A menos que esse item for especificado, o Project Online retorna PublishedProject objetos que não incluem dados de campo personalizado.
    
   - **IncludeCustomFields.CustomFields** &ndash; este item solicita o serviço para preencher os objetos PublishedProject com dados CustomFields.
    
   A solicitação a seguir especifica o Id do projeto e nome, bem como a extensão do objeto para campos personalizados e os valores de campo personalizado.
    
   ```cs
        var projBlk = projContext.LoadQuery(
        projContext.Projects.Include(
            p => p.Id, 
            p => p.Name,
            p => p.IncludeCustomFields,
            p => p.IncludeCustomFields.CustomFields
        ));
    
   ```

3. Examine cada projeto.
    
   Os objetos de projeto usados nesse aplicativo são o tipo de PublishedProject porque os valores são recuperados e exibidos. 
    
   Se você precisar atualizar os valores de dados em um ou mais projetos, o projeto sendo submetido a atualização seria fazer check-out e o aplicativo usaria um objeto DraftProject para recuperar os valores e atualizar o projeto.
    
4. Acessando as entradas ECF para um projeto
    
   Cada instância ECF separa o valor do campo do restante das informações ECF. O valor do campo é armazenado como parte de um par de chave/valor. O restante das informações é armazenado em um objeto CustomField.
    
   Acessar valores de ECF em um projeto consiste em duas partes:
    
   - Percorrendo a coleção CustomFields
    
   - Acessando a entrada adequada usando duas construções.
    
   Cada projeto armazena entradas ECF associadas em dois lugares, um conjunto de CustomFields enumeráveis e e os valores de campo como parte de pares de chave/valor. Nos pares de chave/valor, o internalName é a chave e o valor do campo é o valor. Use um dicionário para manter e acessar os valores de campo. 
    
   As propriedades ECF, que não seja os valores de campo são armazenadas em objetos CustomField, um objeto por projeto. Use um conjunto de CustomFields para acessar os ECFs associados a um projeto individual. 
    
5. Cada projeto armazena os ECFs associados em uma coleção onde cada entrada ECF consiste em uma chave--o nome interno do ECF – e um objeto que contém o valor do ECF. Transferi um dicionário para acessar entradas individuais da coleção. A declaração segue.
    
   ```cs
    Dictionary<string, object> projDict = pubProj.IncludeCustomFields.FieldValues;
    
   ```

   O valor em uma entrada do dicionário corresponde ao tipo de dados do ECF. O objeto para cada ECF mapeado para um dos diversos tipos de. A maioria dos ECFs usam tipos de simples que se encaixam em variáveis standard. O fragmento a seguir mostra que o mínimo de processamento está envolvido para vários tipos:
    
   ```cs
    switch (cf.FieldType)
    {
        case CustomFieldType.COST:
            decimal costValue = (decimal)oVal;
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                costValue.ToString("C"));
            break;
        case CustomFieldType.DATE:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
        case CustomFieldType.FINISHDATE:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
        case CustomFieldType.DURATION:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
        case CustomFieldType.FLAG:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
        case CustomFieldType.NUMBER:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
    
   ```

   A tabela de pesquisa de valores de texto, no entanto, requer processamento adicional. O aplicativo recupera a tabela de pesquisa apropriado do serviço e produz a instância ECF (com um ou vários valores) atravessando a tabela de pesquisa. O fragmento de código a seguir mostra o processamento de texto ECFs, incluindo aqueles que possuem valores simples e aquelas que usam tabelas de pesquisa: 
    
   ```cs
    case CustomFieldType.TEXT:
        if (!cf.LookupTable.ServerObjectIsNull.HasValue ||
            (cf.LookupTable.ServerObjectIsNull.HasValue && 
            cf.LookupTable.ServerObjectIsNull.Value))
        { //No lookup table
            Console.WriteLine("\tFieldType:\t{0}\n\tText:\t{1}", cf.FieldType, 
                oVal.ToString());
        }
        else
        { //Lookup table
            Console.WriteLine("\tFieldType:\t{0} - using Lookup Table", cf.FieldType);
            String[] entries = (String[])oVal;
            foreach (String entry in entries)
            {
                var luEntry = projContext.LoadQuery(cf.LookupTable.Entries
                    .Where(e => e.InternalName == entry));
                projContext.ExecuteQuery();
                Console.WriteLine("\tLookup Value:\t{0}", luEntry.First().FullValue);  
            }
        }
        break;
    
   ```

   Esse aplicativo simplesmente emite o valor (es); No entanto, é possível fazer mais significado a partir do valor de dados (es).
    
## <a name="listpwacustomfields"></a>ListPWACustomFields

O método ListPWACustomFields recupera e lista os ECFs associados aos projetos. Esse método lista os ECFs registrados na instância do PWA que pode ser associada aos projetos individuais. O ponto de entrada para acessar os ECFs usa o elemento CustomFields do contexto do projeto, como a solicitação de consulta a seguir:
  
```cs
// Project ECFs
    var allECFields = 
            projContext.LoadQuery(projContext.CustomFields.Include(
            qp => qp.InternalName,
            qp => qp.Name
        ));
    projContext.ExecuteQuery();

```

O método não verifica para ver se um projeto usa um ECF específico.
  
## <a name="see-also"></a>Confira também

- [Portal de desenvolvimento do Project](https://developer.microsoft.com/en-us/project)
- [Visão geral: Campos personalizados da empresa e tabelas de pesquisa](https://support.office.com/en-us/article/overview-enterprise-custom-fields-and-lookup-tables-f99db553-0b33-4648-93c0-f6a74637d790?ui=en-us&rs=en-us&ad=us)
- [Local e campos personalizados da empresa](https://msdn.microsoft.com/en-us/library/office/ms447495(v=office.14).aspx)
- [Adicionar ou editar campos personalizados empresariais no Project Server 2013](https://docs.microsoft.com/en-us/project/add-or-edit-enterprise-custom-fields-in-project-server)
    

