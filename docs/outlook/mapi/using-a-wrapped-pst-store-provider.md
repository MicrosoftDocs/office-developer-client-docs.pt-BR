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
# <a name="using-a-wrapped-pst-store-provider"></a>Usando um provedor de armazenamento com quebra PST

**Aplica-se a**: Outlook 
  
Antes de poder usar um provedor de armazenamento de arquivo (. PST) de pastas particulares com quebra, você deve inicializar e configurar o provedor de repositórios de PST com quebra. Depois que o provedor de repositórios de PST com quebra estiver configurado, você deve implementar funções para que o spooler MAPI e MAPI podem fazer logon no provedor de armazenamento de mensagem. Para obter mais informações sobre inicializar e fazer logon em um provedor de armazenamento de PST com quebra, consulte [inicializar um provedor de repositório PST quebrado automaticamente](initializing-a-wrapped-pst-store-provider.md) e [Registro em log em um provedor de repositório PST quebrado automaticamente](logging-on-to-a-wrapped-pst-store-provider.md).
  
A interface de **[IMAPISupport::IUnknown](imapisupportiunknown.md)** fornece implementações para tarefas que são executadas por mensagem provedores de armazenamento. Essa interface deve ser quebrada para o Sample quebradas PST Store Provider trabalhar. A função **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** requer a implementação especial. Todas as outras funções podem passar seus parâmetros para o objeto de base com quebra. 
  
Neste tópico, a função **IMAPISupport::OpenProfileSection** é demonstrada usando um exemplo de código a partir do provedor de repositório de PST quebrado automaticamente amostra. O exemplo implementa um provedor de PST com quebra que se destina a ser usado em conjunto com a API de replicação. Para obter mais informações sobre baixando e instalando o provedor de repositórios de PST quebrado automaticamente amostra, consulte [Instalando o provedor de repositórios de PST quebrado automaticamente amostra](installing-the-sample-wrapped-pst-store-provider.md). Para obter mais informações sobre a API de replicação, consulte [Sobre o API de replicação](about-the-replication-api.md).
  
Quando terminar de usar um provedor de armazenamento com quebra PST, você deve desligar adequadamente o provedor de repositórios de PST com quebra. Para obter mais informações, consulte [Sendo pressionada um quebradas PST Store Provider](shutting-down-a-wrapped-pst-store-provider.md).
  
## <a name="open-profile-section-routine"></a>Rotina de seção perfil aberta

A função **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** abre uma seção do perfil atual. A função requer manipulação especial na implementação do provedor de repositório PST com quebra. Quando o `pgNSTGlobalProfileSectionGuid` é solicitada, a função retornará a seção de perfil que é armazenado em cache. 
  
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

- [Sobre o exemplo de provedor do repositório PST encapsulado](about-the-sample-wrapped-pst-store-provider.md)
- [Instalar o provedor do repositório PST encapsulado de exemplo](installing-the-sample-wrapped-pst-store-provider.md)
- [Iniciar um provedor do repositório PST encapsulado](initializing-a-wrapped-pst-store-provider.md)
- [Fazer logon em um provedor do repositório PST encapsulado](logging-on-to-a-wrapped-pst-store-provider.md)
- [Desativar um provedor do repositório PST encapsulado](shutting-down-a-wrapped-pst-store-provider.md)

