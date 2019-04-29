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
# <a name="using-a-wrapped-pst-store-provider"></a>Usar um provedor do repositório PST encapsulado

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Antes de poder usar um provedor de repositório de arquivos de pastas particulares (PST), você deve inicializar e configurar o provedor de repositório PST encapsulado. Após a configuração do provedor de repositório PST encapsulado, você deve implementar as funções para que o MAPI e o spooler MAPI possam fazer logon no provedor de armazenamento de mensagens. Para obter mais informações sobre como inicializar e fazer logon em um provedor de repositório PST encapsulado, consulte [inicializar um provedor de repositório PST encapsulado](initializing-a-wrapped-pst-store-provider.md) e [fazer logon em um provedor de repositório PST encapsulado](logging-on-to-a-wrapped-pst-store-provider.md).
  
A interface **[IMAPISupport:: IUnknown](imapisupportiunknown.md)** fornece implementações para tarefas comumente executadas por provedores de repositório de mensagens. Essa interface deve ser encapsulada para que o provedor de repositório PST encapsulado de exemplo funcione. A função **[IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md)** requer uma implementação especial. Todas as outras funções podem passar seus parâmetros para o objeto wrapped subjacente. 
  
Neste tópico, a função **IMAPISupport:: OpenProfileSection** é demonstrada usando um exemplo de código do provedor de repositório PST encapsulado de amostra. O exemplo implementa um provedor de PST encapsulado destinado a ser usado em conjunto com a API de replicação. Para obter mais informações sobre como baixar e instalar o exemplo de provedor de repositório PST encapsulado, consulte [instalando o provedor de repositório PST encapsulado de amostra](installing-the-sample-wrapped-pst-store-provider.md). Para obter mais informações sobre a API de replicação, consulte [About The Replication API](about-the-replication-api.md).
  
Ao concluir o uso de um provedor de repositório PST encapsulado, você deve desligar corretamente o provedor de repositório PST encapsulado. Para obter mais informações, consulte desLigamento [de um provedor de armazenamento PST encapsulado](shutting-down-a-wrapped-pst-store-provider.md).
  
## <a name="open-profile-section-routine"></a>Rotina abrir seção de perfil

A função **[IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md)** abre uma seção do perfil atual. A função requer tratamento especial na implementação do provedor de repositório PST encapsulado. Quando a `pgNSTGlobalProfileSectionGuid` solicitação é solicitada, a função retorna a seção de perfil armazenada em cache. 
  
### <a name="csupportopenprofilesection-example"></a>Exemplo de CSupport:: OpenProfileSection ()

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

- [Sobre o exemplo de provedor de repositório PST encapsulado](about-the-sample-wrapped-pst-store-provider.md)
- [Instalando o provedor de repositório PST encapsulado de exemplo](installing-the-sample-wrapped-pst-store-provider.md)
- [Inicializando um provedor de repositório PST encapsulado](initializing-a-wrapped-pst-store-provider.md)
- [Fazer logon em um provedor de repositório PST encapsulado](logging-on-to-a-wrapped-pst-store-provider.md)
- [DesLigamento de um provedor de repositório PST encapsulado](shutting-down-a-wrapped-pst-store-provider.md)

