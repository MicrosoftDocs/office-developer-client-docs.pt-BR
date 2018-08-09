---
title: Biblioteca de JavaScript e referência do restante do Project Server
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 67b47b8b-d34b-4fad-af49-0c258c345ad2
description: A biblioteca JavaScript e REST referenciarem para o Project Server 2013 contém informações sobre o modelo de objeto JavaScript e a interface REST que você usa para acessar a funcionalidade do Project Server. Você pode usar essas APIs para desenvolver aplicativos para dispositivos não-Windows que acessam o Project Server 2013 e Project Online, suplementos do Project Professional 2013 e vários navegadores web apps.
ms.openlocfilehash: f834ffdc80de28eceb2d7ab9b30c1444b0478bd8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771059"
---
# <a name="javascript-library-and-rest-reference-for-project-server"></a>Biblioteca de JavaScript e referência do restante do Project Server

A biblioteca JavaScript e REST referenciarem para o Project Server 2013 contém informações sobre o modelo de objeto JavaScript e a interface REST que você usa para acessar a funcionalidade do Project Server. Você pode usar essas APIs para desenvolver aplicativos para dispositivos não-Windows que acessam o Project Server 2013 e Project Online, suplementos do Project Professional 2013 e vários navegadores web apps.
  
> [!NOTE]
> O modelo de objeto JavaScript e a interface REST alinhados com o modelo de objeto do cliente (CSOM) do Project Server. Eles fornecem funcionalidade equivalente ao namespace **Microsoft.ProjectServer.Client** no CSOM. 
  
Você pode acessar a funcionalidade do Project Server através do modelo de objeto JavaScript, que é definido no namespace [PS](http://msdn.microsoft.com/library/e3156167-a4fd-1bf6-8d1c-e180de1844ed%28Office.15%29.aspx) no `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\PS.js` arquivo. O objeto [ProjectContext](http://msdn.microsoft.com/library/a490b675-a845-ee94-3877-b99ada9bf2b0%28Office.15%29.aspx) no namespace [PS](http://msdn.microsoft.com/library/e3156167-a4fd-1bf6-8d1c-e180de1844ed%28Office.15%29.aspx) é o ponto de entrada para o modelo de objeto JavaScript. 
  
> [!NOTE]
> Para procurar o modelo de objeto JavaScript e ajuda na depuração, você pode usar o arquivo PS.debug.js no mesmo diretório. Para ajudar no desenvolvimento em um computador remoto, o [SDK do Project 2013 download](https://www.microsoft.com/en-us/download/details.aspx?id=30435) inclui os assemblies do .NET Framework para o CSOM e os arquivos PS.js e PS.debug.js. 
  
Você também pode acessar a funcionalidade do Project Server por meio da interface REST. O ponto de partida para a interface REST é o recurso de **ProjectServer** , que você acessa usando o `http://ServerName/pwaName/_api/ProjectServer` URI do ponto de extremidade. Por exemplo, a consulta a seguir obtém as atribuições no projeto especificado (substitua _ServerName_ e _pwaName_e alterar o GUID para fazer a correspondência de um projeto).
  
`http://ServerName/pwaName/_api/ProjectServer/Projects('263fc8d7-427c-e111-92fc-00155d3ba208')/Assignments`

O recurso **ProjectServer** é descrito em [recursos ProjectServer a interface REST](http://msdn.microsoft.com/library/a490b675-a845-ee94-3877-b99ada9bf2b0%28Office.15%29.aspx#bk_ProjectServerResources). Outros recursos REST são descritos na documentação para os objetos correspondentes do JavaScript e membros nesta referência. Para obter mais informações sobre como usar o REST, consulte [o modelo de objeto do lado do cliente (CSOM) para o Project Server](client-side-object-model-csom-for-project-2013.md) e [programação usando o serviço REST do SharePoint 2013](http://msdn.microsoft.com/en-us/library/fp142385%28office.15%29.aspx).
  
## <a name="javascript-library-and-rest-reference-for-project-server"></a>Biblioteca de JavaScript e referência do restante do Project Server
<a name="pj15_JavaScriptAPIReference_PS"> </a>

- [Referência do REST e biblioteca PS.js JavaScript](http://msdn.microsoft.com/library/5a140021-380a-d9e0-e36d-106df85f56d6%28Office.15%29.aspx) Contém informações sobre o modelo de objeto JavaScript e a interface REST do Project Server 2013. 
    
## <a name="see-also"></a>Confira também
<a name="bk_addresources"> </a>

- [Documentação do desenvolvedor do Project 2013](project-2013-developer-documentation.md)   
- [Modelo de objeto do cliente (CSOM) para o Project Server](client-side-object-model-csom-for-project-2013.md)   
- [Introdução ao modelo de objeto do JavaScript](getting-started-with-the-project-server-2013-javascript-object-model.md)  
- [Trabalhar com projetos usando o modelo de objeto do JavaScript](create-retrieve-update-delete-projects-using-project-server-javascript.md)
    

