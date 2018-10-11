---
title: Referência do REST e da biblioteca de JavaScript no Project Server
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 67b47b8b-d34b-4fad-af49-0c258c345ad2
description: A biblioteca de JavaScript e a referência REST para o Project Server 2013 contém informações sobre o modelo de objeto e sobre a interface RESt que você usa para acessar as funcionalidades do JavaScript. Você pode usar esses APIs para desenvolver aplicativos em vários navegadores da web, suplementos do Project Professional 2013 e aplicativos para dispositivos que não sejam do Windows para acessar o Project Server 2013 e no Project Online.
ms.openlocfilehash: fb58de1e3858a39f42cc9a643a7394cec191a462
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399029"
---
# <a name="javascript-library-and-rest-reference-for-project-server"></a>Referência do REST e da biblioteca de JavaScript no Project Server

A biblioteca de JavaScript e a referência REST para o Project Server 2013 contém informações sobre o modelo de objeto e sobre a interface RESt que você usa para acessar as funcionalidades do JavaScript. Você pode usar esses APIs para desenvolver aplicativos em vários navegadores da web, suplementos do Project Professional 2013 e aplicativos para dispositivos que não sejam do Windows para acessar o Project Server 2013 e no Project Online.
  
> [!NOTE]
> O modelo de objeto do JavaScript e a interface REST se alinham com o modelo de objeto do lado do cliente do Project Server (CSOM). É possível fornecer a funcionalidade equivalente para o namespace**Microsoft.ProjectServer.Client**no CSOM. 
  
Você pode acessar a funcionalidade do Project Server através do modelo de objeto do JavaScript, definido no namespace [PS](https://msdn.microsoft.com/library/e3156167-a4fd-1bf6-8d1c-e180de1844ed%28Office.15%29.aspx)do `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\PS.js` arquivo. O objeto[ProjectContext](https://msdn.microsoft.com/library/a490b675-a845-ee94-3877-b99ada9bf2b0%28Office.15%29.aspx)no namespace [PS](https://msdn.microsoft.com/library/e3156167-a4fd-1bf6-8d1c-e180de1844ed%28Office.15%29.aspx)é o ponto de entrada para o modelo de objeto do JavaScript. 
  
> [!NOTE]
> Para procurar um modelo de objeto do JavaScript e ajudar a depuração de bugs, você pode usar o arquivo PS.debug.js na mesma pasta. Para ajudar o desenvolvimento em um computador remoto, o [download do Project 2013 SDK](https://www.microsoft.com/en-us/download/details.aspx?id=30435) inclui conjuntos do .NET Framework para o CSOM e os arquivos PS.js e PS.debug.js. 
  
Você também pode acessar as funcionalidades do Project Server por meio da interface do REST. O ponto de entrada para a interface do REST é o recurso**ProjectServer** que pode ser acessada usando o`https://ServerName/pwaName/_api/ProjectServer` ponto de extremidade URI. Por exemplo, a seguinte consulta obtém as tarefas do projeto especificado (substitua _NomeServidor_ e _pwaName_e altere o GUID para corresponder a um projeto).
  
`https://ServerName/pwaName/_api/ProjectServer/Projects('263fc8d7-427c-e111-92fc-00155d3ba208')/Assignments`

O recurso**ProjectServer** é descrito em [recursos ProjectServer recursos na interface REST](https://msdn.microsoft.com/library/a490b675-a845-ee94-3877-b99ada9bf2b0%28Office.15%29.aspx#bk_ProjectServerResources). Outros recursos REST estão descritos na documentação de objetos de JavaScript correspondentes e nos membros essa referência. Para mais informações sobre como usar o REST, confira[modelo de objeto do cliente (CSOM) para o Project Server](client-side-object-model-csom-for-project-2013.md) e [programação usando o serviço REST do SharePoint 2013](https://msdn.microsoft.com/library/fp142385%28office.15%29.aspx).
  
## <a name="javascript-library-and-rest-reference-for-project-server"></a>Referência do REST e da biblioteca de JavaScript no Project Server
<a name="pj15_JavaScriptAPIReference_PS"> </a>

- [A biblioteca de JavaScript e a referência REST](https://msdn.microsoft.com/library/5a140021-380a-d9e0-e36d-106df85f56d6%28Office.15%29.aspx)contém informações sobre o modelo de objeto e sobre a interface REST que você usa para o Project Server 2013. 
    
## <a name="see-also"></a>Confira também
<a name="bk_addresources"> </a>

- [Documentação do desenvolvedor do Project 2013](project-2013-developer-documentation.md)   
- [Modelo de objeto do cliente (CSOM) para o Project Server](client-side-object-model-csom-for-project-2013.md)   
- [Introdução ao modelo de objeto do JavaScript](getting-started-with-the-project-server-2013-javascript-object-model.md)  
- [Trabalhar com projetos usando o modelo de objeto do JavaScript](create-retrieve-update-delete-projects-using-project-server-javascript.md)
    

