---
title: Acessar campos personalizados da empresa no Project Online
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
ms.assetid: 25509631-fa14-49d8-b594-cfacf5355c38
description: 'O Project Online é um serviço do Office 365 que as empresas podem estender para atender às necessidades de negócios. Uma área de extensão são os Campos Personalizados da Empresa (Enterprise Custom Fields – ECFs). Os ECFs são campos de valores tipados que podem ser adicionados a projetos, recursos e tarefas. A tabela a seguir lista os ECFs que se associam a projetos, recursos e tarefas e fornece um exemplo de um valor para uma instância desse ECF:'
localization_priority: Priority
ms.openlocfilehash: 9f754f1446890ae021bf6f7000ffba11e2a2df33
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355080"
---
# <a name="accessing-project-online-enterprise-custom-fields"></a>Acessar campos personalizados da empresa no Project Online

O Project Online é um serviço do Office 365 que as empresas podem estender para atender às necessidades de negócios. Uma área de extensão são os Campos Personalizados da Empresa (Enterprise Custom Fields – ECFs). Os ECFs são campos de valores tipados que podem ser adicionados a projetos, recursos e tarefas. A tabela a seguir lista os ECFs que se associam a projetos, recursos e tarefas e fornece um exemplo de um valor para uma instância desse ECF:
  
|Nome ECF|Tipo ECF|Association|Valor de Exemplo|
|:-----|:-----|:-----|:-----|
|Justificação  <br/> |TEXTO  <br/> |Project  <br/> |Um usuário final pode registrar estatísticas vitais e dados sobre a integridade, com resultados que incluem uma avaliação da integridade e um plano de ação individualizado para melhorá-la.  <br/> |
|Classificação de risco  <br/> |TEXTO  <br/> |Project  <br/> |Baixo  <br/> |
|ROI  <br/> |NÚMERO  <br/> |Project  <br/> |2,10  <br/> |
|Custo total  <br/> |CUSTO  <br/> |Project  <br/> |US$ 1.031.514  <br/> |
|Equipe de lançamento  <br/> |TEXTO  <br/> |Recursos  <br/> |Sim  <br/> |
|Função de posição  <br/> |TEXTO  <br/> |Recursos  <br/> |Testador  <br/> |
|Status do sinalizador  <br/> |SINALIZAR  <br/> |Tarefa  <br/> |Não  <br/> |
|Integridade  <br/> |TEXTO  <br/> |Tarefa  <br/> |Não especificado  <br/> |
   
Os ECFs são definidos na instância externa do Project Web Application (PWA), de qualquer projeto, recurso ou tarefa. No entanto, eles podem se associar a um projeto, recurso ou tarefa. Este artigo fornece uma visão introdutória dos campos personalizados usando um aplicativo de exemplo e se concentra na recuperação de valores do ECF. 
  
É possível baixar o exemplo completo em https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields.
  
Além disso, o Project Online é compatível com campos personalizados locais como entidades somente leitura específicas para o projeto, recursos ou tarefa específico. Para saber mais sobre campos personalizados locais, confira o exemplo https://github.com/OfficeDev/Project-CSOM-Read-Local-CustomFields\.
  
## <a name="background-materials"></a>Materiais de tela de fundo

Um artigo anterior, [Desenvolver um aplicativo do Project Online usando o modelo de objeto do lado do cliente](developing-a-project-online-application-using-the-client-side-object-model.md), fornece o plano de fundo e a orientação inicial para o desenvolvimento de aplicativos usando o CSOM. Confira este artigo para ver os seguintes itens:
  
- Informações sobre o Project, edições autônomas e baseadas na nuvem 
    
- Ambiente de desenvolvimento (edições do Visual Studio e bibliotecas de software)
    
- Instalação do projeto do Visual Studio para um aplicativo .NET usando a biblioteca CSOM
    
- Conexão com o serviço do Project Online
    
## <a name="preliminaries-class-level-declarations"></a>Preliminares (declarações de nível de classe)

A classe deste aplicativo define dois itens de dados: o contexto do projeto e o dicionário pwaECF.
  
O objeto do contexto do projeto faz parte do CSOM Project e conecta instância PWA e o aplicativo. Todas as solicitações do serviço usam o contexto do projeto.
  
```cs
private static ProjectContext projContext = 
     new ProjectContext("https://Contoso216.sharepoint.com/sites/pwa");

```

O contexto precisa do ponto de extremidade de conexão para criar uma instância em um aplicativo. O ponto de extremidade de conexão é a URL de sua instância do PWA. 
  
O dicionário pwaECF armazena os EFCs do projeto definidos no nível do PWA. O dicionário usa o ECF.InternalName como a chave e o objeto CustomField como o valor. O dicionário é preenchido no método ListPWACustomFields e, em seguida, é usado como uma referência no método Main. 
  
```cs
    //Dictionary of ECFs
        static Dictionary<String, CustomField> pwaECF = new Dictionary<string, CustomField>();

```

## <a name="main-method"></a>Método Main

O método Main gerencia o fluxo do aplicativo. Assim como em outros aplicativos que usam o CSOM do Project Online, o Main inicializa o contexto do projeto. 
  
1. Recupere e liste os ECFs no PWA do Project Online.
    
   Esse recurso é implementado no método ListPWACustomFields.
    
2. Recupere projetos com campos personalizados e campos não personalizados.
    
   Ao recuperar projetos com ECFs, a solicitação de consulta feita ao serviço do Project Online deve incluir os seguintes itens: 
    
   - **IncludeCustomFields** &ndash; Este item solicita que o serviço retorne uma coleção de PublishedProjects, em que cada projeto publicado inclui uma extensão que oferece suporte a campos personalizados. A menos que este item seja especificado, o Project Online retorna objetos PublishedProject que não incluem dados do campo personalizado.
    
   - **IncludeCustomFields.CustomFields** &ndash; Este item solicita que o serviço preencha os objetos PublishedProject com dados de CustomFields.
    
   A solicitação a seguir especifica a ID e o nome do projeto, além da extensão do objeto para campos personalizados e os valores do campo personalizado.
    
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
    
   Os objetos de projeto usados neste aplicativo são do tipo PublishedProject porque os valores são recuperados e exibidos. 
    
   Se você precisar atualizar valores de dados em um ou mais projetos, o projeto que está passando pela atualização passará por check-out e o aplicativo utilizará um objeto DraftProject para recuperar os valores e atualizar o projeto.
    
4. Acessar as entradas ECF para um projeto
    
   Cada instância do ECF separa o valor do campo do restante das informações do ECF. O valor do campo é armazenado como parte de um par de chave/valor. O restante das informações é armazenado em um objeto CustomField.
    
   O acesso a valores do ECF em um projeto consiste em duas partes:
    
   - Passar pela coleção CustomFields
    
   - Acessar a entrada adequada usando duas construções.
    
   Cada projeto armazena entradas do ECF associadas em dois locais, uma coleção CustomFields que é enumerável e os valores do campo como parte de pares de chave/valor. Em pares de chave/valor, o internalName é a chave e o valor do campo é o valor. Use um dicionário para armazenar e acessar os valores do campo. 
    
   As propriedades do ECF, além dos valores de campo, são armazenadas em objetos CustomField, um objeto por projeto. Use uma coleção CustomFields para acessar os ECFs associados a um projeto individual. 
    
5. Cada projeto armazena os ECFs associados em uma coleção na qual cada entrada do ECF é formada por uma chave, o nome interno do ECF, e um objeto que contém o valor do ECF. Transfira a coleção para um dicionário para acessar entradas individuais. A declaração seguirá a transferência.
    
   ```cs
    Dictionary<string, object> projDict = pubProj.IncludeCustomFields.FieldValues;
    
   ```

   O valor em uma entrada de dicionário corresponde ao tipo de dados do ECF. O objeto para cada ECF é mapeado para um dos vários tipos. A maioria dos ECFs usa tipos simples que se encaixam em variáveis padrão. O fragmento a seguir mostra que o processamento mínimo está envolvido em vários tipos:
    
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

   A tabela de pesquisa de valores de TEXTO, no entanto, requer processamento adicional. O aplicativo recupera a tabela de consulta apropriada do serviço e gera a instância do ECF (com valores únicos ou múltiplos) percorrendo a tabela de consulta. O fragmento de código a seguir mostra o processamento de ECFs de TEXTO, incluindo aqueles com valores simples e aqueles que usam tabelas de consulta: 
    
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

   Este aplicativo simplesmente mostra os valores. No entanto, é possível obter mais significado nos valores de dados.
    
## <a name="listpwacustomfields"></a>ListPWACustomFields

O método ListPWACustomFields recupera e lista ECFs associados a projetos. Esse método lista ECFs registrados na instância PWA que pode ser associada a projetos individuais. O ponto de entrada para acessar os ECFs usa o elemento CustomFields do contexto do projeto, como na solicitação de consulta a seguir:
  
```cs
// Project ECFs
    var allECFields = 
            projContext.LoadQuery(projContext.CustomFields.Include(
            qp => qp.InternalName,
            qp => qp.Name
        ));
    projContext.ExecuteQuery();

```

O método não verifica se um projeto usa um ECF específico.
  
## <a name="see-also"></a>Confira também

- [Plataforma de desenvolvimento do Project](https://developer.microsoft.com/pt-BR/project)
- [Visão geral: campos personalizados empresariais e tabelas de pesquisa](https://support.office.com/en-us/article/overview-enterprise-custom-fields-and-lookup-tables-f99db553-0b33-4648-93c0-f6a74637d790?ui=en-us&rs=en-us&ad=us)
- [Campos personalizados empresariais e locais](https://msdn.microsoft.com/library/office/ms447495(v=office.14).aspx)
- [Adicionar ou editar campos personalizados empresariais no Project Server 2013](https://docs.microsoft.com/project/add-or-edit-enterprise-custom-fields-in-project-server)
    

