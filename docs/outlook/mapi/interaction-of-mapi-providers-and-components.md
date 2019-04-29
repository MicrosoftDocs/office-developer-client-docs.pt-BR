---
title: Interação de provedores e componentes MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c0e010b-0432-4ef7-a243-3a4b46f0a19d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b88eafcc1ca6be98c5c1e9418072a5cb35f43345
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434659"
---
# <a name="interaction-of-mapi-providers-and-components"></a><span data-ttu-id="232b9-103">Interação de provedores e componentes MAPI</span><span class="sxs-lookup"><span data-stu-id="232b9-103">Interaction of MAPI Providers and Components</span></span>

  
  
<span data-ttu-id="232b9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="232b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="232b9-105">Os provedores de serviço MAPI de qualquer tipo devem seguir algumas diretrizes para trabalhar com outros componentes MAPI.</span><span class="sxs-lookup"><span data-stu-id="232b9-105">MAPI service providers of any kind must follow certain guidelines to work with other MAPI components.</span></span> <span data-ttu-id="232b9-106">Cada provedor de serviços deve:</span><span class="sxs-lookup"><span data-stu-id="232b9-106">Each service provider must:</span></span>
  
- <span data-ttu-id="232b9-107">Use o provedor e os objetos de logon adequados para inicialização.</span><span class="sxs-lookup"><span data-stu-id="232b9-107">Use the proper provider and logon objects for initialization.</span></span>
    
- <span data-ttu-id="232b9-108">Retornar uma tabela de expedição de pontos de entrada de provedor para o sistema de mensagens na inicialização.</span><span class="sxs-lookup"><span data-stu-id="232b9-108">Return a dispatch table of provider entry points to the messaging system upon initialization.</span></span>
    
- <span data-ttu-id="232b9-109">Registre uma linha de tabela de status MAPI para cada recurso pertencente ao provedor e chame o método [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) em momentos apropriados.</span><span class="sxs-lookup"><span data-stu-id="232b9-109">Register a MAPI status table row for each resource owned by the provider and call the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method at appropriate times.</span></span> 
    
- <span data-ttu-id="232b9-110">Use o método [IMAPISupport:: NewUID](imapisupport-newuid.md) para obter UIDs (identificadores exclusivos) válidos.</span><span class="sxs-lookup"><span data-stu-id="232b9-110">Use the [IMAPISupport::NewUID](imapisupport-newuid.md) method to obtain valid unique identifiers (UIDs).</span></span> 
    
- <span data-ttu-id="232b9-111">Suportar as interfaces comuns de MAPI em objetos que ele retorna.</span><span class="sxs-lookup"><span data-stu-id="232b9-111">Support the common MAPI interfaces on objects it returns.</span></span>
    
- <span data-ttu-id="232b9-112">Use as funções de alocação de memória MAPI para alocar memória retornada aos aplicativos cliente e para liberar a memória alocada por outras partes do subsistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="232b9-112">Use the MAPI memory allocation functions to allocate memory returned to client applications and to release memory allocated by other parts of the MAPI subsystem.</span></span>
    
- <span data-ttu-id="232b9-113">Mantenha uma seção de perfil, se necessário, para armazenar credenciais para o sistema de mensagens subjacente.</span><span class="sxs-lookup"><span data-stu-id="232b9-113">Maintain a profile section, if necessary, to store credentials to the underlying messaging system.</span></span>
    
- <span data-ttu-id="232b9-114">Use o método [IMAPISupport:: RegisterPreprocessor](imapisupport-registerpreprocessor.md) para registrar qualquer função de pré-processamento de mensagem.</span><span class="sxs-lookup"><span data-stu-id="232b9-114">Use the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method to register any message preprocessing functions.</span></span> 
    
- <span data-ttu-id="232b9-115">Inclua os arquivos de cabeçalho adequados (incluindo mapispi. h) que definem constantes, estruturas, interfaces e valores de retorno comuns.</span><span class="sxs-lookup"><span data-stu-id="232b9-115">Include the proper header files (including mapispi.h) that define common constants, structures, interfaces, and return values.</span></span>
    
- <span data-ttu-id="232b9-116">Siga as convenções de formato de endereço para tipos de endereço comuns.</span><span class="sxs-lookup"><span data-stu-id="232b9-116">Follow address format conventions for common address types.</span></span>
    

