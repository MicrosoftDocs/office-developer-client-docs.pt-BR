---
title: Desativar um provedor do repositório PST encapsulado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0c9e5917-1b96-323d-bf8b-1d3aa1f677d0
description: 'Modificado pela última vez: 02 de julho de 2012'
ms.openlocfilehash: 43a65548bedc1729ff2bcb62bc3df78d2408bf12
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571742"
---
# <a name="shutting-down-a-wrapped-pst-store-provider"></a><span data-ttu-id="b73f3-103">Desativar um provedor do repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="b73f3-103">Shutting Down a Wrapped PST Store Provider</span></span>

 
  
<span data-ttu-id="b73f3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b73f3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b73f3-105">Após concluir o uso de um provedor de armazenamento de arquivo (. PST) de pastas particulares com quebra, você deve desligar corretamente o provedor de repositórios de PST com quebra.</span><span class="sxs-lookup"><span data-stu-id="b73f3-105">After you finish using a wrapped Personal Folders file (PST) store provider, you must properly shut down the wrapped PST store provider.</span></span> <span data-ttu-id="b73f3-106">Para obter mais informações sobre como usar o provedor de repositórios de PST com quebra, consulte [usando um provedor de repositório PST quebrado automaticamente](using-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b73f3-106">For more information about using the wrapped PST store provider, see [Using a Wrapped PST Store Provider](using-a-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="b73f3-107">Para encerrar um provedor de armazenamento com quebra PST, você deve chamar a função **[IMSProvider::Shutdown](imsprovider-shutdown.md)** .</span><span class="sxs-lookup"><span data-stu-id="b73f3-107">To shut down a wrapped PST store provider, you must call the **[IMSProvider::Shutdown](imsprovider-shutdown.md)** function.</span></span> <span data-ttu-id="b73f3-108">Este funções encerra o provedor de repositórios de PST com quebra de forma ordenada.</span><span class="sxs-lookup"><span data-stu-id="b73f3-108">This functions closes down the wrapped PST store provider in an orderly fashion.</span></span> 
  
<span data-ttu-id="b73f3-109">Neste tópico, a função **IMSProvider::Shutdown** é demonstrada usando um exemplo de código a partir do provedor de repositório de PST quebrado automaticamente amostra.</span><span class="sxs-lookup"><span data-stu-id="b73f3-109">In this topic, the **IMSProvider::Shutdown** function is demonstrated by using a code example from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="b73f3-110">O exemplo implementa um provedor de PST com quebra que se destina a ser usado em conjunto com a API de replicação.</span><span class="sxs-lookup"><span data-stu-id="b73f3-110">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="b73f3-111">Para obter mais informações sobre baixando e instalando o provedor de repositórios de PST quebrado automaticamente amostra, consulte [Instalando o provedor de repositórios de PST quebrado automaticamente amostra](installing-the-sample-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b73f3-111">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="b73f3-112">Para obter mais informações sobre a API de replicação, consulte [Sobre o API de replicação](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="b73f3-112">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
## <a name="shut-down-routine"></a><span data-ttu-id="b73f3-113">Desligue a rotina</span><span class="sxs-lookup"><span data-stu-id="b73f3-113">Shut Down Routine</span></span>

<span data-ttu-id="b73f3-114">O MAPI spooler chama a função de **[IMSProvider::Shutdown](imsprovider-shutdown.md)** antes de ele libera o provedor de repositórios de PST com quebra para que o provedor de repositórios de PST com quebra pode desligar corretamente.</span><span class="sxs-lookup"><span data-stu-id="b73f3-114">The MAPI spooler calls the **[IMSProvider::Shutdown](imsprovider-shutdown.md)** function just before it releases the wrapped PST store provider so that the wrapped PST store provider can shut down properly.</span></span> <span data-ttu-id="b73f3-115">A função finaliza todos os objetos de sessão associados com o provedor de repositórios de PST com quebra.</span><span class="sxs-lookup"><span data-stu-id="b73f3-115">The function terminates all session objects associated with the wrapped PST store provider.</span></span> 
  
## <a name="cmsprovidershutdown-example"></a><span data-ttu-id="b73f3-116">Exemplo de CMSProvider::ShutDown()</span><span class="sxs-lookup"><span data-stu-id="b73f3-116">CMSProvider::ShutDown() Example</span></span>

```cpp
STDMETHODIMP CMSProvider::Shutdown(ULONG * pulFlags) 
{ 
    HRESULT hRes = S_OK; 
    Log(true,"CMSProvider::Shutdown\n"); 
    hRes =m_pPSTMS->Shutdown(pulFlags); 
    Log(true,"CMSProvider::Shutdown returned: 0x%08X\n", hRes); 
    return hRes ;  
}
```

## <a name="see-also"></a><span data-ttu-id="b73f3-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="b73f3-117">See also</span></span>



[<span data-ttu-id="b73f3-118">Sobre o exemplo de provedor do repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="b73f3-118">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="b73f3-119">Instalar o provedor do repositório PST encapsulado de exemplo</span><span class="sxs-lookup"><span data-stu-id="b73f3-119">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="b73f3-120">Iniciar um provedor do repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="b73f3-120">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="b73f3-121">Fazer logon em um provedor do repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="b73f3-121">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="b73f3-122">Usar um provedor do repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="b73f3-122">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)

