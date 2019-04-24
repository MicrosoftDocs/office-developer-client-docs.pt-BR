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
# <a name="shutting-down-a-wrapped-pst-store-provider"></a>DesLigamento de um provedor de repositório PST encapsulado

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Depois de concluir o uso de um provedor de repositório de arquivos de pastas particulares (PST), você deve desligar corretamente o provedor de repositório PST encapsulado. Para obter mais informações sobre como usar o provedor de repositório PST encapsulado, consulte [usando um provedor de repositório PST encapsulado](using-a-wrapped-pst-store-provider.md).
  
Para desligar um provedor de repositório PST encapsulado, você deve chamar a função **[IMSProvider:: Shutdown](imsprovider-shutdown.md)** . Essa função fecha o provedor de repositório PST encapsulado de maneira ordenada. 
  
Neste tópico, a função **IMSProvider:: Shutdown** é demonstrada usando um exemplo de código do provedor de repositório PST encapsulado de amostra. O exemplo implementa um provedor de PST encapsulado destinado a ser usado em conjunto com a API de replicação. Para obter mais informações sobre como baixar e instalar o exemplo de provedor de repositório PST encapsulado, consulte [instalando o provedor de repositório PST encapsulado de amostra](installing-the-sample-wrapped-pst-store-provider.md). Para obter mais informações sobre a API de replicação, consulte [About The Replication API](about-the-replication-api.md).
  
## <a name="shut-down-routine"></a>Rotina de desLigamento

O spooler MAPI chama a função **[IMSProvider:: Shutdown](imsprovider-shutdown.md)** imediatamente antes de liberar o provedor de repositório PST encapsulado para que o provedor de repositório PST encapsulado possa ser desligado corretamente. A função encerra todos os objetos de sessão associados ao provedor de repositório PST encapsulado. 
  
## <a name="cmsprovidershutdown-example"></a>Exemplo de CMSProvider:: ShutDown ()

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



[Sobre o exemplo de provedor de repositório PST encapsulado](about-the-sample-wrapped-pst-store-provider.md)
  
[Instalando o provedor de repositório PST encapsulado de exemplo](installing-the-sample-wrapped-pst-store-provider.md)
  
[Inicializando um provedor de repositório PST encapsulado](initializing-a-wrapped-pst-store-provider.md)
  
[Fazer logon em um provedor de repositório PST encapsulado](logging-on-to-a-wrapped-pst-store-provider.md)
  
[Usando um provedor de repositório PST encapsulado](using-a-wrapped-pst-store-provider.md)

