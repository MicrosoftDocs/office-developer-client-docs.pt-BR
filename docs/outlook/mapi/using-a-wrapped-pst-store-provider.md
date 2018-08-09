---
title: Usando um provedor de armazenamento com quebra PST
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 98f08432-e86c-cba6-45fd-5a6c94d50aaf
description: 'Modificado pela última vez: 03 de julho de 2012'
ms.openlocfilehash: 4a2ccbbcdd3459af6b69156d80b37695251ba8d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770686"
---
# <a name="using-a-wrapped-pst-store-provider"></a><span data-ttu-id="5f51f-103">Usando um provedor de armazenamento com quebra PST</span><span class="sxs-lookup"><span data-stu-id="5f51f-103">Using a wrapped PST store provider</span></span>

<span data-ttu-id="5f51f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5f51f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5f51f-105">Antes de poder usar um provedor de armazenamento de arquivo (. PST) de pastas particulares com quebra, você deve inicializar e configurar o provedor de repositórios de PST com quebra.</span><span class="sxs-lookup"><span data-stu-id="5f51f-105">Before you can use a wrapped Personal Folders file (PST) store provider, you must initialize and configure the wrapped PST store provider.</span></span> <span data-ttu-id="5f51f-106">Depois que o provedor de repositórios de PST com quebra estiver configurado, você deve implementar funções para que o spooler MAPI e MAPI podem fazer logon no provedor de armazenamento de mensagem.</span><span class="sxs-lookup"><span data-stu-id="5f51f-106">After the wrapped PST store provider is configured, you must implement functions so that MAPI and the MAPI spooler can log on to the message store provider.</span></span> <span data-ttu-id="5f51f-107">Para obter mais informações sobre inicializar e fazer logon em um provedor de armazenamento de PST com quebra, consulte [inicializar um provedor de repositório PST quebrado automaticamente](initializing-a-wrapped-pst-store-provider.md) e [Registro em log em um provedor de repositório PST quebrado automaticamente](logging-on-to-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="5f51f-107">For more information about initializing and logging on to a wrapped PST store provider, see [Initializing a Wrapped PST Store Provider](initializing-a-wrapped-pst-store-provider.md) and [Logging On to a Wrapped PST Store Provider](logging-on-to-a-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="5f51f-108">A interface de **[IMAPISupport::IUnknown](imapisupportiunknown.md)** fornece implementações para tarefas que são executadas por mensagem provedores de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5f51f-108">The **[IMAPISupport::IUnknown](imapisupportiunknown.md)** interface provides implementations for tasks that are commonly performed by message store providers.</span></span> <span data-ttu-id="5f51f-109">Essa interface deve ser quebrada para o Sample quebradas PST Store Provider trabalhar.</span><span class="sxs-lookup"><span data-stu-id="5f51f-109">This interface must be wrapped for the Sample Wrapped PST Store Provider to work.</span></span> <span data-ttu-id="5f51f-110">A função **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** requer a implementação especial.</span><span class="sxs-lookup"><span data-stu-id="5f51f-110">The **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** function requires special implementation.</span></span> <span data-ttu-id="5f51f-111">Todas as outras funções podem passar seus parâmetros para o objeto de base com quebra.</span><span class="sxs-lookup"><span data-stu-id="5f51f-111">All other functions can pass their parameters to the underlying wrapped object.</span></span> 
  
<span data-ttu-id="5f51f-112">Neste tópico, a função **IMAPISupport::OpenProfileSection** é demonstrada usando um exemplo de código a partir do provedor de repositório de PST quebrado automaticamente amostra.</span><span class="sxs-lookup"><span data-stu-id="5f51f-112">In this topic, the **IMAPISupport::OpenProfileSection** function is demonstrated by using a code example from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="5f51f-113">O exemplo implementa um provedor de PST com quebra que se destina a ser usado em conjunto com a API de replicação.</span><span class="sxs-lookup"><span data-stu-id="5f51f-113">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="5f51f-114">Para obter mais informações sobre baixando e instalando o provedor de repositórios de PST quebrado automaticamente amostra, consulte [Instalando o provedor de repositórios de PST quebrado automaticamente amostra](installing-the-sample-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="5f51f-114">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="5f51f-115">Para obter mais informações sobre a API de replicação, consulte [Sobre o API de replicação](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="5f51f-115">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="5f51f-116">Quando terminar de usar um provedor de armazenamento com quebra PST, você deve desligar adequadamente o provedor de repositórios de PST com quebra.</span><span class="sxs-lookup"><span data-stu-id="5f51f-116">When you finish using a wrapped PST store provider, you must properly shut down the wrapped PST store provider.</span></span> <span data-ttu-id="5f51f-117">Para obter mais informações, consulte [Sendo pressionada um quebradas PST Store Provider](shutting-down-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="5f51f-117">For more information, see [Shutting Down a Wrapped PST Store Provider](shutting-down-a-wrapped-pst-store-provider.md).</span></span>
  
## <a name="open-profile-section-routine"></a><span data-ttu-id="5f51f-118">Rotina de seção perfil aberta</span><span class="sxs-lookup"><span data-stu-id="5f51f-118">Open Profile Section routine</span></span>

<span data-ttu-id="5f51f-119">A função **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** abre uma seção do perfil atual.</span><span class="sxs-lookup"><span data-stu-id="5f51f-119">The **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** function opens a section of the current profile.</span></span> <span data-ttu-id="5f51f-120">A função requer manipulação especial na implementação do provedor de repositório PST com quebra.</span><span class="sxs-lookup"><span data-stu-id="5f51f-120">The function requires special handling in the wrapped PST store provider implementation.</span></span> <span data-ttu-id="5f51f-121">Quando o `pgNSTGlobalProfileSectionGuid` é solicitada, a função retornará a seção de perfil que é armazenado em cache.</span><span class="sxs-lookup"><span data-stu-id="5f51f-121">When the  `pgNSTGlobalProfileSectionGuid` is requested, the function returns the profile section that is cached.</span></span> 
  
### <a name="csupportopenprofilesection-example"></a><span data-ttu-id="5f51f-122">Exemplo de CSupport::OpenProfileSection()</span><span class="sxs-lookup"><span data-stu-id="5f51f-122">CSupport::OpenProfileSection() example</span></span>

```cpp
STDMETHODIMP CSupport::OpenProfileSection( 
    LPMAPIUID lpUid,     
    ULONG ulFlags, 
    LPPROFSECT * lppProfileObj) 
{ 
    Log(true,"CSupport::OpenProfileSection\n"); 
    if (lpUid &&  
        IsEqualMAPIUID(lpUid, (void *)&pbNSTGlobalProfileSectionGuid) &&  
        m_lpProfSect) 
    {      
        // Allow the opening of the Global Section 
        if (m_lpProfSect) 
        { 
            *lppProfileObj = m_lpProfSect; 
            (*lppProfileObj)->AddRef(); 
            return S_OK; 
        } 
    } 
    return m_pMAPISup->OpenProfileSection(lpUid, ulFlags, lppProfileObj); 
}
```

## <a name="see-also"></a><span data-ttu-id="5f51f-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="5f51f-123">See also</span></span>

- [<span data-ttu-id="5f51f-124">Sobre o exemplo de provedor do repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="5f51f-124">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
- [<span data-ttu-id="5f51f-125">Instalar o provedor do repositório PST encapsulado de exemplo</span><span class="sxs-lookup"><span data-stu-id="5f51f-125">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md)
- [<span data-ttu-id="5f51f-126">Iniciar um provedor do repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="5f51f-126">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="5f51f-127">Fazer logon em um provedor do repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="5f51f-127">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="5f51f-128">Desativar um provedor do repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="5f51f-128">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

