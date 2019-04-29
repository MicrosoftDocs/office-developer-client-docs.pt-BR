---
title: Recuperar propriedades do formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9dec5ad6-af34-4c5e-848b-5c3909d0c0a1
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 023d2cf312438b1e4b6a90c57e1ead7d606d7727
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412916"
---
# <a name="retrieving-form-properties"></a><span data-ttu-id="f3386-103">Recuperar propriedades do formulário</span><span class="sxs-lookup"><span data-stu-id="f3386-103">Retrieving Form Properties</span></span>

  
  
<span data-ttu-id="f3386-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f3386-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f3386-105">Para emitir uma consulta que seja significativa para um tipo de mensagem personalizada, um aplicativo precisa saber as propriedades esperadas nessa mensagem.</span><span class="sxs-lookup"><span data-stu-id="f3386-105">To issue a query that is meaningful to a custom message type, an application needs to know the properties that are expected on that message.</span></span> <span data-ttu-id="f3386-106">Para obter uma lista de propriedades que uma classe de mensagem personalizada usa, um aplicativo cliente consulta o Gerenciador de formulários MAPI.</span><span class="sxs-lookup"><span data-stu-id="f3386-106">To get a list of properties that a custom message class uses, a client application queries the MAPI form manager.</span></span> <span data-ttu-id="f3386-107">O gerente de formulários obtém essas informações do arquivo de configuração de formulário apropriado para que os aplicativos clientes possam usar essas informações sem a sobrecarga de ativar o próprio servidor de formulário.</span><span class="sxs-lookup"><span data-stu-id="f3386-107">The form manager gets this information from the appropriate form configuration file so that client applications can use this information without the overhead of activating the form server itself.</span></span> <span data-ttu-id="f3386-108">Para fazer isso, o aplicativo cliente chama o método [IMAPIFormMgr:: ResolveMessageClass](imapiformmgr-resolvemessageclass.md) da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="f3386-108">To do this, the client application calls the [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) method as follows:</span></span> 
  
```cpp
IMAPIFormInfo *pfrminf = NULL;
hr = pfrmmgr->ResolveMessageClass("IPM.Demo", 0L, NULL, &amp;pfrminf);

```

<span data-ttu-id="f3386-109">Observe que o terceiro argumento para **ResolveMessageClass** é a pasta que contém a tabela de conteúdo associada que a consulta pesquisará para servidores de formulário.</span><span class="sxs-lookup"><span data-stu-id="f3386-109">Note that the third argument to **ResolveMessageClass** is the folder that contains the associated contents table that the query will search for form servers.</span></span> <span data-ttu-id="f3386-110">NULL indica que o gerente de formulários deve pesquisar todos os contêineres de formulário disponíveis.</span><span class="sxs-lookup"><span data-stu-id="f3386-110">NULL indicates that the form manager should search all available form containers.</span></span> <span data-ttu-id="f3386-111">Se a consulta for executada em uma determinada pasta, é melhor incluir o ponteiro [IMAPIFolder](imapifolderimapicontainer.md) apropriado.</span><span class="sxs-lookup"><span data-stu-id="f3386-111">If the query is to run against a particular folder, it is better to include the appropriate [IMAPIFolder](imapifolderimapicontainer.md) pointer instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f3386-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="f3386-112">See also</span></span>



[<span data-ttu-id="f3386-113">InterAções do servidor de formulário</span><span class="sxs-lookup"><span data-stu-id="f3386-113">Form Server Interactions</span></span>](form-server-interactions.md)

