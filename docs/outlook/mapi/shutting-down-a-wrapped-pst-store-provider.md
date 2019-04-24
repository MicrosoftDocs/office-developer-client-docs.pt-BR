---
title: DesLigamento de um provedor de repositório PST encapsulado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0c9e5917-1b96-323d-bf8b-1d3aa1f677d0
description: 'Última modificação: 02 de julho de 2012'
ms.openlocfilehash: fa918920213ee77c4d0c1d3ccc239ae7cffe81fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282779"
---
# <a name="shutting-down-a-wrapped-pst-store-provider"></a><span data-ttu-id="71e8b-103">DesLigamento de um provedor de repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="71e8b-103">Shutting Down a Wrapped PST Store Provider</span></span>

 
  
<span data-ttu-id="71e8b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="71e8b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="71e8b-105">Depois de concluir o uso de um provedor de repositório de arquivos de pastas particulares (PST), você deve desligar corretamente o provedor de repositório PST encapsulado.</span><span class="sxs-lookup"><span data-stu-id="71e8b-105">After you finish using a wrapped Personal Folders file (PST) store provider, you must properly shut down the wrapped PST store provider.</span></span> <span data-ttu-id="71e8b-106">Para obter mais informações sobre como usar o provedor de repositório PST encapsulado, consulte [usando um provedor de repositório PST encapsulado](using-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="71e8b-106">For more information about using the wrapped PST store provider, see [Using a Wrapped PST Store Provider](using-a-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="71e8b-107">Para desligar um provedor de repositório PST encapsulado, você deve chamar a função **[IMSProvider:: Shutdown](imsprovider-shutdown.md)** .</span><span class="sxs-lookup"><span data-stu-id="71e8b-107">To shut down a wrapped PST store provider, you must call the **[IMSProvider::Shutdown](imsprovider-shutdown.md)** function.</span></span> <span data-ttu-id="71e8b-108">Essa função fecha o provedor de repositório PST encapsulado de maneira ordenada.</span><span class="sxs-lookup"><span data-stu-id="71e8b-108">This functions closes down the wrapped PST store provider in an orderly fashion.</span></span> 
  
<span data-ttu-id="71e8b-109">Neste tópico, a função **IMSProvider:: Shutdown** é demonstrada usando um exemplo de código do provedor de repositório PST encapsulado de amostra.</span><span class="sxs-lookup"><span data-stu-id="71e8b-109">In this topic, the **IMSProvider::Shutdown** function is demonstrated by using a code example from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="71e8b-110">O exemplo implementa um provedor de PST encapsulado destinado a ser usado em conjunto com a API de replicação.</span><span class="sxs-lookup"><span data-stu-id="71e8b-110">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="71e8b-111">Para obter mais informações sobre como baixar e instalar o exemplo de provedor de repositório PST encapsulado, consulte [instalando o provedor de repositório PST encapsulado de amostra](installing-the-sample-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="71e8b-111">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="71e8b-112">Para obter mais informações sobre a API de replicação, consulte [About The Replication API](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="71e8b-112">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
## <a name="shut-down-routine"></a><span data-ttu-id="71e8b-113">Rotina de desLigamento</span><span class="sxs-lookup"><span data-stu-id="71e8b-113">Shut Down Routine</span></span>

<span data-ttu-id="71e8b-114">O spooler MAPI chama a função **[IMSProvider:: Shutdown](imsprovider-shutdown.md)** imediatamente antes de liberar o provedor de repositório PST encapsulado para que o provedor de repositório PST encapsulado possa ser desligado corretamente.</span><span class="sxs-lookup"><span data-stu-id="71e8b-114">The MAPI spooler calls the **[IMSProvider::Shutdown](imsprovider-shutdown.md)** function just before it releases the wrapped PST store provider so that the wrapped PST store provider can shut down properly.</span></span> <span data-ttu-id="71e8b-115">A função encerra todos os objetos de sessão associados ao provedor de repositório PST encapsulado.</span><span class="sxs-lookup"><span data-stu-id="71e8b-115">The function terminates all session objects associated with the wrapped PST store provider.</span></span> 
  
## <a name="cmsprovidershutdown-example"></a><span data-ttu-id="71e8b-116">Exemplo de CMSProvider:: ShutDown ()</span><span class="sxs-lookup"><span data-stu-id="71e8b-116">CMSProvider::ShutDown() Example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="71e8b-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="71e8b-117">See also</span></span>



[<span data-ttu-id="71e8b-118">Sobre o exemplo de provedor de repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="71e8b-118">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="71e8b-119">Instalando o provedor de repositório PST encapsulado de exemplo</span><span class="sxs-lookup"><span data-stu-id="71e8b-119">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="71e8b-120">Inicializando um provedor de repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="71e8b-120">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="71e8b-121">Fazer logon em um provedor de repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="71e8b-121">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="71e8b-122">Usando um provedor de repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="71e8b-122">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)

