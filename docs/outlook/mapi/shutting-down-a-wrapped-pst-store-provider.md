---
title: Desligar um provedor de armazenamento PST empacotado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0c9e5917-1b96-323d-bf8b-1d3aa1f677d0
description: 'Last modified: July 02, 2012'
ms.openlocfilehash: fa918920213ee77c4d0c1d3ccc239ae7cffe81fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409941"
---
# <a name="shutting-down-a-wrapped-pst-store-provider"></a>Desligar um provedor de armazenamento PST empacotado

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Depois de terminar de usar um provedor de armazenamento de Pastas Particulares (PST), você deve desligar corretamente o provedor do armazenamento PST. Para obter mais informações sobre como usar o provedor de armazenamento PST empacotado, consulte [Usando um provedor de armazenamento PST.](using-a-wrapped-pst-store-provider.md)
  
Para desligar um provedor de armazenamento PST empacotado, você deve chamar a **[função IMSProvider::Shutdown.](imsprovider-shutdown.md)** Essas funções fecham o provedor de armazenamento PST empacotado de forma pedido. 
  
Neste tópico, a função **IMSProvider::Shutdown** é demonstrada usando um exemplo de código do Sample Wrapped PST Store Provider. O exemplo implementa um provedor PST empacotado que se destina a ser usado em conjunto com a API de Replicação. Para obter mais informações sobre como baixar e instalar o Sample Wrapped PST Store Provider, consulte [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md). Para obter mais informações sobre a API de Replicação, consulte [Sobre a API de Replicação.](about-the-replication-api.md)
  
## <a name="shut-down-routine"></a>Rotina de desligar

O spooler MAPI chama a função **[IMSProvider::Shutdown](imsprovider-shutdown.md)** antes de liberar o provedor de armazenamento PST empacotado para que o provedor de armazenamento PST empacotado possa desligar corretamente. A função encerra todos os objetos de sessão associados ao provedor de armazenamento PST empacotado. 
  
## <a name="cmsprovidershutdown-example"></a>Exemplo de CMSProvider::ShutDown()

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

## <a name="see-also"></a>Confira também



[Sobre o provedor de armazenamento PST com conteúdo de exemplo](about-the-sample-wrapped-pst-store-provider.md)
  
[Instalando o provedor de armazenamento PST com conteúdo de exemplo](installing-the-sample-wrapped-pst-store-provider.md)
  
[Inicializando um provedor de armazenamento PST empacotado](initializing-a-wrapped-pst-store-provider.md)
  
[Logondo em um provedor de armazenamento PST empacotado](logging-on-to-a-wrapped-pst-store-provider.md)
  
[Usando um provedor de armazenamento PST empacotado](using-a-wrapped-pst-store-provider.md)

