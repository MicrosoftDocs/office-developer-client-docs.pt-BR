---
title: Usar um provedor do repositório PST encapsulado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 98f08432-e86c-cba6-45fd-5a6c94d50aaf
description: 'Última modificação: 03 de julho de 2012'
ms.openlocfilehash: b7c651044ab7f4cad7032db69e157c9a3589bde9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420819"
---
# <a name="using-a-wrapped-pst-store-provider"></a><span data-ttu-id="d37f1-103">Usar um provedor do repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="d37f1-103">Using a wrapped PST store provider</span></span>

<span data-ttu-id="d37f1-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d37f1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d37f1-105">Antes de poder usar um provedor de repositório de arquivos de pastas particulares (PST), você deve inicializar e configurar o provedor de repositório PST encapsulado.</span><span class="sxs-lookup"><span data-stu-id="d37f1-105">Before you can use a wrapped Personal Folders file (PST) store provider, you must initialize and configure the wrapped PST store provider.</span></span> <span data-ttu-id="d37f1-106">Após a configuração do provedor de repositório PST encapsulado, você deve implementar as funções para que o MAPI e o spooler MAPI possam fazer logon no provedor de armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="d37f1-106">After the wrapped PST store provider is configured, you must implement functions so that MAPI and the MAPI spooler can log on to the message store provider.</span></span> <span data-ttu-id="d37f1-107">Para obter mais informações sobre como inicializar e fazer logon em um provedor de repositório PST encapsulado, consulte [inicializar um provedor de repositório PST encapsulado](initializing-a-wrapped-pst-store-provider.md) e [fazer logon em um provedor de repositório PST encapsulado](logging-on-to-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="d37f1-107">For more information about initializing and logging on to a wrapped PST store provider, see [Initializing a Wrapped PST Store Provider](initializing-a-wrapped-pst-store-provider.md) and [Logging On to a Wrapped PST Store Provider](logging-on-to-a-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="d37f1-108">A interface **[IMAPISupport:: IUnknown](imapisupportiunknown.md)** fornece implementações para tarefas comumente executadas por provedores de repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="d37f1-108">The **[IMAPISupport::IUnknown](imapisupportiunknown.md)** interface provides implementations for tasks that are commonly performed by message store providers.</span></span> <span data-ttu-id="d37f1-109">Essa interface deve ser encapsulada para que o provedor de repositório PST encapsulado de exemplo funcione.</span><span class="sxs-lookup"><span data-stu-id="d37f1-109">This interface must be wrapped for the Sample Wrapped PST Store Provider to work.</span></span> <span data-ttu-id="d37f1-110">A função **[IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md)** requer uma implementação especial.</span><span class="sxs-lookup"><span data-stu-id="d37f1-110">The **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** function requires special implementation.</span></span> <span data-ttu-id="d37f1-111">Todas as outras funções podem passar seus parâmetros para o objeto wrapped subjacente.</span><span class="sxs-lookup"><span data-stu-id="d37f1-111">All other functions can pass their parameters to the underlying wrapped object.</span></span> 
  
<span data-ttu-id="d37f1-112">Neste tópico, a função **IMAPISupport:: OpenProfileSection** é demonstrada usando um exemplo de código do provedor de repositório PST encapsulado de amostra.</span><span class="sxs-lookup"><span data-stu-id="d37f1-112">In this topic, the **IMAPISupport::OpenProfileSection** function is demonstrated by using a code example from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="d37f1-113">O exemplo implementa um provedor de PST encapsulado destinado a ser usado em conjunto com a API de replicação.</span><span class="sxs-lookup"><span data-stu-id="d37f1-113">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="d37f1-114">Para obter mais informações sobre como baixar e instalar o exemplo de provedor de repositório PST encapsulado, consulte [instalando o provedor de repositório PST encapsulado de amostra](installing-the-sample-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="d37f1-114">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="d37f1-115">Para obter mais informações sobre a API de replicação, consulte [About The Replication API](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="d37f1-115">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="d37f1-116">Ao concluir o uso de um provedor de repositório PST encapsulado, você deve desligar corretamente o provedor de repositório PST encapsulado.</span><span class="sxs-lookup"><span data-stu-id="d37f1-116">When you finish using a wrapped PST store provider, you must properly shut down the wrapped PST store provider.</span></span> <span data-ttu-id="d37f1-117">Para obter mais informações, consulte desLigamento [de um provedor de armazenamento PST encapsulado](shutting-down-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="d37f1-117">For more information, see [Shutting Down a Wrapped PST Store Provider](shutting-down-a-wrapped-pst-store-provider.md).</span></span>
  
## <a name="open-profile-section-routine"></a><span data-ttu-id="d37f1-118">Rotina abrir seção de perfil</span><span class="sxs-lookup"><span data-stu-id="d37f1-118">Open Profile Section routine</span></span>

<span data-ttu-id="d37f1-119">A função **[IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md)** abre uma seção do perfil atual.</span><span class="sxs-lookup"><span data-stu-id="d37f1-119">The **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** function opens a section of the current profile.</span></span> <span data-ttu-id="d37f1-120">A função requer tratamento especial na implementação do provedor de repositório PST encapsulado.</span><span class="sxs-lookup"><span data-stu-id="d37f1-120">The function requires special handling in the wrapped PST store provider implementation.</span></span> <span data-ttu-id="d37f1-121">Quando a `pgNSTGlobalProfileSectionGuid` solicitação é solicitada, a função retorna a seção de perfil armazenada em cache.</span><span class="sxs-lookup"><span data-stu-id="d37f1-121">When the  `pgNSTGlobalProfileSectionGuid` is requested, the function returns the profile section that is cached.</span></span> 
  
### <a name="csupportopenprofilesection-example"></a><span data-ttu-id="d37f1-122">Exemplo de CSupport:: OpenProfileSection ()</span><span class="sxs-lookup"><span data-stu-id="d37f1-122">CSupport::OpenProfileSection() example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="d37f1-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="d37f1-123">See also</span></span>

- [<span data-ttu-id="d37f1-124">Sobre o exemplo de provedor de repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="d37f1-124">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
- [<span data-ttu-id="d37f1-125">Instalando o provedor de repositório PST encapsulado de exemplo</span><span class="sxs-lookup"><span data-stu-id="d37f1-125">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md)
- [<span data-ttu-id="d37f1-126">Inicializando um provedor de repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="d37f1-126">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="d37f1-127">Fazer logon em um provedor de repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="d37f1-127">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="d37f1-128">DesLigamento de um provedor de repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="d37f1-128">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

