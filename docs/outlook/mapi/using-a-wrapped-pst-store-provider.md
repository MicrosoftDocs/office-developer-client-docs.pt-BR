---
title: Usar um provedor do repositório PST encapsulado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 98f08432-e86c-cba6-45fd-5a6c94d50aaf
description: 'Last modified: July 03, 2012'
ms.openlocfilehash: b7c651044ab7f4cad7032db69e157c9a3589bde9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420819"
---
# <a name="using-a-wrapped-pst-store-provider"></a>Usar um provedor do repositório PST encapsulado

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Antes de poder usar um provedor de armazenamento de Pastas Particulares (PST) empacotado, você deve inicializar e configurar o provedor de armazenamento PST. Depois que o provedor de armazenamento PST empacotado estiver configurado, você deverá implementar funções para que o MAPI e o spooler MAPI possam fazer logoff no provedor de armazenamento de mensagens. Para obter mais informações sobre como inicializar e fazer logo login em um provedor de armazenamento PST empacotado, consulte Inicializando um provedor de armazenamento [PST](initializing-a-wrapped-pst-store-provider.md) com envoltório e logondo em um provedor de armazenamento [PST.](logging-on-to-a-wrapped-pst-store-provider.md)
  
A interface **[IMAPISupport::IUnknown](imapisupportiunknown.md)** fornece implementações para tarefas normalmente executadas por provedores de armazenamento de mensagens. Essa interface deve ser empacotada para que o Provedor de Armazenamento PST com Conteúdo de Exemplo funcione. A **[função IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** requer implementação especial. Todas as outras funções podem passar seus parâmetros para o objeto de empacotado subjacente. 
  
Neste tópico, a função **IMAPISupport::OpenProfileSection** é demonstrada usando um exemplo de código do Sample Wrapped PST Store Provider. O exemplo implementa um provedor PST empacotado que se destina a ser usado em conjunto com a API de Replicação. Para obter mais informações sobre como baixar e instalar o Sample Wrapped PST Store Provider, consulte [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md). Para obter mais informações sobre a API de Replicação, consulte [Sobre a API de Replicação.](about-the-replication-api.md)
  
Quando terminar de usar um provedor de armazenamento PST empacotado, você deve desligar corretamente o provedor de armazenamento PST empacotado. Para obter mais informações, [consulte Desligar um provedor de armazenamento PST.](shutting-down-a-wrapped-pst-store-provider.md)
  
## <a name="open-profile-section-routine"></a>Rotina abrir seção de perfil

A **[função IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** abre uma seção do perfil atual. A função requer um tratamento especial na implementação do provedor de armazenamento PST. Quando  `pgNSTGlobalProfileSectionGuid` solicitado, a função retorna a seção de perfil armazenada em cache. 
  
### <a name="csupportopenprofilesection-example"></a>Exemplo de CSupport::OpenProfileSection()

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

## <a name="see-also"></a>Confira também

- [Sobre o provedor de armazenamento PST com conteúdo de exemplo](about-the-sample-wrapped-pst-store-provider.md)
- [Instalando o provedor de armazenamento PST com conteúdo de exemplo](installing-the-sample-wrapped-pst-store-provider.md)
- [Inicializando um provedor de armazenamento PST empacotado](initializing-a-wrapped-pst-store-provider.md)
- [Fazendo logom em um provedor de armazenamento PST empacotado](logging-on-to-a-wrapped-pst-store-provider.md)
- [Desligar um provedor de armazenamento PST empacotado](shutting-down-a-wrapped-pst-store-provider.md)

