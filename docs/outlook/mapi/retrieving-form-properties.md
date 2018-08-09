---
title: Recuperar propriedades do formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9dec5ad6-af34-4c5e-848b-5c3909d0c0a1
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 334ecaacec88c3730f4cc2f4c80eb35d5a553c4e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770270"
---
# <a name="retrieving-form-properties"></a><span data-ttu-id="93357-103">Recuperar propriedades do formulário</span><span class="sxs-lookup"><span data-stu-id="93357-103">Retrieving Form Properties</span></span>

  
  
<span data-ttu-id="93357-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="93357-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="93357-105">Para emitir uma consulta que é significativa para um tipo de mensagem personalizado, um aplicativo que precisa saber as propriedades esperados sobre a mensagem.</span><span class="sxs-lookup"><span data-stu-id="93357-105">To issue a query that is meaningful to a custom message type, an application needs to know the properties that are expected on that message.</span></span> <span data-ttu-id="93357-106">Para obter uma lista de propriedades que usa uma classe de mensagem personalizada, um aplicativo cliente consulta o Gerenciador de formulário MAPI.</span><span class="sxs-lookup"><span data-stu-id="93357-106">To get a list of properties that a custom message class uses, a client application queries the MAPI form manager.</span></span> <span data-ttu-id="93357-107">O gerente do formulário obtém essas informações do arquivo de configuração de formulário apropriada para que os aplicativos cliente podem usar essas informações sem a sobrecarga de ativação do servidor de formulário em si.</span><span class="sxs-lookup"><span data-stu-id="93357-107">The form manager gets this information from the appropriate form configuration file so that client applications can use this information without the overhead of activating the form server itself.</span></span> <span data-ttu-id="93357-108">Para fazer isso, o aplicativo cliente chama o método [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="93357-108">To do this, the client application calls the [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) method as follows:</span></span> 
  
```cpp
IMAPIFormInfo *pfrminf = NULL;
hr = pfrmmgr->ResolveMessageClass("IPM.Demo", 0L, NULL, &amp;pfrminf);

```

<span data-ttu-id="93357-109">Observe que o terceiro argumento para **ResolveMessageClass** é a pasta que contém a tabela de conteúdo associado que a consulta buscarão para servidores de formulário.</span><span class="sxs-lookup"><span data-stu-id="93357-109">Note that the third argument to **ResolveMessageClass** is the folder that contains the associated contents table that the query will search for form servers.</span></span> <span data-ttu-id="93357-110">NADA indica que o Gerenciador de formulário deve pesquisar todos os contêineres do formulário disponível.</span><span class="sxs-lookup"><span data-stu-id="93357-110">NULL indicates that the form manager should search all available form containers.</span></span> <span data-ttu-id="93357-111">Se a consulta deve ser executado em uma pasta particular, é melhor incluir o ponteiro de [IMAPIFolder](imapifolderimapicontainer.md) apropriado em vez disso.</span><span class="sxs-lookup"><span data-stu-id="93357-111">If the query is to run against a particular folder, it is better to include the appropriate [IMAPIFolder](imapifolderimapicontainer.md) pointer instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="93357-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="93357-112">See also</span></span>



[<span data-ttu-id="93357-113">Interações do servidor de formulário</span><span class="sxs-lookup"><span data-stu-id="93357-113">Form Server Interactions</span></span>](form-server-interactions.md)

