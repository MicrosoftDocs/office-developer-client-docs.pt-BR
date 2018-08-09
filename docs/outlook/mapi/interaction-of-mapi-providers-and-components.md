---
title: Interação de provedores e componentes MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c0e010b-0432-4ef7-a243-3a4b46f0a19d
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: cb0f8d5077b4851a50ceb8523943ae760a8ee5ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767590"
---
# <a name="interaction-of-mapi-providers-and-components"></a><span data-ttu-id="139ca-103">Interação de provedores e componentes MAPI</span><span class="sxs-lookup"><span data-stu-id="139ca-103">Interaction of MAPI Providers and Components</span></span>

  
  
<span data-ttu-id="139ca-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="139ca-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="139ca-105">Provedores de serviço MAPI de qualquer tipo devem seguir determinadas diretrizes para trabalhar com outros componentes MAPI.</span><span class="sxs-lookup"><span data-stu-id="139ca-105">MAPI service providers of any kind must follow certain guidelines to work with other MAPI components.</span></span> <span data-ttu-id="139ca-106">Cada provedor de serviços deve:</span><span class="sxs-lookup"><span data-stu-id="139ca-106">Each service provider must:</span></span>
  
- <span data-ttu-id="139ca-107">Use os objetos de logon e o provedor adequados para inicialização.</span><span class="sxs-lookup"><span data-stu-id="139ca-107">Use the proper provider and logon objects for initialization.</span></span>
    
- <span data-ttu-id="139ca-108">Retorne uma tabela de expedição de pontos de entrada do provedor para o sistema de mensagens na inicialização.</span><span class="sxs-lookup"><span data-stu-id="139ca-108">Return a dispatch table of provider entry points to the messaging system upon initialization.</span></span>
    
- <span data-ttu-id="139ca-109">Registrar uma linha de tabela de status MAPI para cada recurso pertencente ao provedor e chamar o método [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) em momentos apropriados.</span><span class="sxs-lookup"><span data-stu-id="139ca-109">Register a MAPI status table row for each resource owned by the provider and call the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method at appropriate times.</span></span> 
    
- <span data-ttu-id="139ca-110">Use o método [IMAPISupport::NewUID](imapisupport-newuid.md) para obter identificadores exclusivos válidos (UIDs).</span><span class="sxs-lookup"><span data-stu-id="139ca-110">Use the [IMAPISupport::NewUID](imapisupport-newuid.md) method to obtain valid unique identifiers (UIDs).</span></span> 
    
- <span data-ttu-id="139ca-111">Suporte para as interfaces MAPI comuns em objetos que ela retorna.</span><span class="sxs-lookup"><span data-stu-id="139ca-111">Support the common MAPI interfaces on objects it returns.</span></span>
    
- <span data-ttu-id="139ca-112">Use as funções de alocação de memória MAPI para alocar memória retornada para aplicativos cliente e para liberar memória alocada por outras partes do subsistema de MAPI.</span><span class="sxs-lookup"><span data-stu-id="139ca-112">Use the MAPI memory allocation functions to allocate memory returned to client applications and to release memory allocated by other parts of the MAPI subsystem.</span></span>
    
- <span data-ttu-id="139ca-113">Manter uma seção de perfil, se necessário, para armazenar credenciais para o sistema de mensagens subjacente.</span><span class="sxs-lookup"><span data-stu-id="139ca-113">Maintain a profile section, if necessary, to store credentials to the underlying messaging system.</span></span>
    
- <span data-ttu-id="139ca-114">Use o método [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) para registrar qualquer mensagem de pré-processamento funções.</span><span class="sxs-lookup"><span data-stu-id="139ca-114">Use the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method to register any message preprocessing functions.</span></span> 
    
- <span data-ttu-id="139ca-115">Inclua os arquivos de cabeçalho adequadas (incluindo mapispi.h) que definem as constantes comuns, estruturas, interfaces e valores de retorno.</span><span class="sxs-lookup"><span data-stu-id="139ca-115">Include the proper header files (including mapispi.h) that define common constants, structures, interfaces, and return values.</span></span>
    
- <span data-ttu-id="139ca-116">Siga as convenções de formato de endereço para tipos de endereço comuns.</span><span class="sxs-lookup"><span data-stu-id="139ca-116">Follow address format conventions for common address types.</span></span>
    

