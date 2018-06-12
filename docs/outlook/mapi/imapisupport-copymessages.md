---
title: IMAPISupportCopyMessages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CopyMessages
api_type:
- COM
ms.assetid: 70f67614-af0d-43f6-99f6-391a2f5673cb
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 64b2c147acb02b6c29cf080076b6fe2e3eefb717
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767215"
---
# <a name="imapisupportcopymessages"></a>IMAPISupport::CopyMessages

  
  
**Aplica-se a**: Outlook 
  
Cópias ou movimentações de mensagens de uma pasta para outra pasta.
  
```cpp
HRESULT CopyMessages(
  LPCIID lpSrcInterface,
  LPVOID lpSrcFolder,
  LPENTRYLIST lpMsgList,
  LPCIID lpDestInterface,
  LPVOID lpDestFolder,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Par�metros

 _lpSrcInterface_
  
> [in] Um ponteiro para o identificador de interface (IID) que representa a interface para ser usado para acessar a pasta que contém as mensagens devem ser copiados ou movidos.
    
 _lpSrcFolder_
  
> [in] Um ponteiro para a pasta que contém as mensagens devem ser copiados ou movidos.
    
 _lpMsgList_
  
> [in] Um ponteiro para uma matriz de identificadores de entrada que identificam as mensagens devem ser copiados ou movidos. 
    
 _lpDestInterface_
  
> [in] Um ponteiro para o identificador de interface (IID) que representa a interface para ser usado para acessar a pasta de destino para as mensagens copiadas ou movidas.
    
 _lpDestFolder_
  
> [in] Um ponteiro para a pasta de destino para as mensagens copiadas ou movidas. Essa pasta deve ser aberta.
    
 _ulUIParam_
  
> [in] Um ponteiro para um objeto de progresso que exibe um indicador de progresso. Se NULL for passado _lpProgress_, o provedor de armazenamento de mensagem exibe um indicador de progresso usando a implementação de objeto de progresso MAPI. O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador MESSAGE_DIALOG está definido na _ulFlags_.
    
 _lpProgress_
  
> [in] Um ponteiro para um objeto de progresso que exibe um indicador de progresso. Se NULL for passado _lpProgress_, o provedor de armazenamento de mensagem exibe um indicador de progresso usando a implementação de objeto de progresso MAPI. O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador MESSAGE_DIALOG está definido na _ulFlags_.
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como a operação de cópia ou movimentação é realizada. Sinalizadores a seguir podem ser definidos:
    
MESSAGE_DIALOG 
  
> Solicita a exibição de um indicador de progresso.
    
MESSAGE_MOVE 
  
> As mensagens devem ser movidas, em vez de copiados. Se MESSAGE_MOVE não estiver definida, as mensagens serão copiadas.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A operação de cópia ou movimentação foi bem-sucedida.
    
MAPI_E_USER_CANCEL 
  
> O usuário cancelou a operação, geralmente clicando no botão **Cancelar** em uma caixa de diálogo. 
    
## <a name="remarks"></a>Coment�rios

O método **IMAPISupport::CopyMessages** é implementado para objetos de suporte do provedor de repositório de mensagem. Provedores de armazenamento de mensagens podem chamar **IMAPISupport::CopyMessages** na sua implementação do [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) para copiar ou mover uma ou mais mensagens de uma pasta para outro. Como parte da chamada **IMAPISupport::CopyMessages** , o provedor de armazenamento de mensagens pode especificar que o MAPI deve exibir um indicador de progresso. 
  
## <a name="see-also"></a>Confira também



[IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

