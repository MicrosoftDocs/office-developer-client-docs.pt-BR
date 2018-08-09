---
title: Desativar um provedor do repositório PST encapsulado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0c9e5917-1b96-323d-bf8b-1d3aa1f677d0
description: 'Modificado pela última vez: 02 de julho de 2012'
ms.openlocfilehash: 5c8ad7443b0c1aa05f48284e4b09859ab53dd2c3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770402"
---
# <a name="shutting-down-a-wrapped-pst-store-provider"></a>Desativar um provedor do repositório PST encapsulado

 
  
**Aplica-se a**: Outlook 
  
Após concluir o uso de um provedor de armazenamento de arquivo (. PST) de pastas particulares com quebra, você deve desligar corretamente o provedor de repositórios de PST com quebra. Para obter mais informações sobre como usar o provedor de repositórios de PST com quebra, consulte [usando um provedor de repositório PST quebrado automaticamente](using-a-wrapped-pst-store-provider.md).
  
Para encerrar um provedor de armazenamento com quebra PST, você deve chamar a função **[IMSProvider::Shutdown](imsprovider-shutdown.md)** . Este funções encerra o provedor de repositórios de PST com quebra de forma ordenada. 
  
Neste tópico, a função **IMSProvider::Shutdown** é demonstrada usando um exemplo de código a partir do provedor de repositório de PST quebrado automaticamente amostra. O exemplo implementa um provedor de PST com quebra que se destina a ser usado em conjunto com a API de replicação. Para obter mais informações sobre baixando e instalando o provedor de repositórios de PST quebrado automaticamente amostra, consulte [Instalando o provedor de repositórios de PST quebrado automaticamente amostra](installing-the-sample-wrapped-pst-store-provider.md). Para obter mais informações sobre a API de replicação, consulte [Sobre o API de replicação](about-the-replication-api.md).
  
## <a name="shut-down-routine"></a>Desligue a rotina

O MAPI spooler chama a função de **[IMSProvider::Shutdown](imsprovider-shutdown.md)** antes de ele libera o provedor de repositórios de PST com quebra para que o provedor de repositórios de PST com quebra pode desligar corretamente. A função finaliza todos os objetos de sessão associados com o provedor de repositórios de PST com quebra. 
  
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



[Sobre o exemplo de provedor do repositório PST encapsulado](about-the-sample-wrapped-pst-store-provider.md)
  
[Instalar o provedor do repositório PST encapsulado de exemplo](installing-the-sample-wrapped-pst-store-provider.md)
  
[Iniciar um provedor do repositório PST encapsulado](initializing-a-wrapped-pst-store-provider.md)
  
[Fazer logon em um provedor do repositório PST encapsulado](logging-on-to-a-wrapped-pst-store-provider.md)
  
[Usar um provedor do repositório PST encapsulado](using-a-wrapped-pst-store-provider.md)

