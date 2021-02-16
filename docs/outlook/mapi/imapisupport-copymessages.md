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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 9cc4e3ba77395e09a6b95e8381fa402fc3cdff61
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405153"
---
# <a name="imapisupportcopymessages"></a>IMAPISupport::CopyMessages

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Copia ou move mensagens de uma pasta para outra.
  
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

## <a name="parameters"></a>Parâmetros

 _lpSrcInterface_
  
> [in] Um ponteiro para o IID (identificador de interface) que representa a interface a ser usada para acessar a pasta que contém as mensagens a serem copiadas ou movidas.
    
 _lpSrcFolder_
  
> [in] Um ponteiro para a pasta que contém as mensagens a serem copiadas ou movidas.
    
 _lpMsgList_
  
> [in] Um ponteiro para uma matriz de identificadores de entrada que identificam as mensagens a serem copiadas ou movidas. 
    
 _lpDestInterface_
  
> [in] Um ponteiro para o IID (identificador de interface) que representa a interface a ser usada para acessar a pasta de destino das mensagens copiadas ou movidas.
    
 _lpDestFolder_
  
> [in] Um ponteiro para a pasta de destino das mensagens copiadas ou movidas. Essa pasta deve estar aberta.
    
 _ulUIParam_
  
> [in] Um ponteiro para um objeto de progresso que exibe um indicador de progresso. Se NULL for passado  _em lpProgress_, o provedor de armazenamento de mensagens exibirá um indicador de progresso usando a implementação de objeto de progresso MAPI. O  _parâmetro lpProgress_ é ignorado, a menos que o sinalizador MESSAGE_DIALOG seja definido em  _ulFlags_.
    
 _lpProgress_
  
> [in] Um ponteiro para um objeto de progresso que exibe um indicador de progresso. Se NULL for passado  _em lpProgress_, o provedor de armazenamento de mensagens exibirá um indicador de progresso usando a implementação de objeto de progresso MAPI. O  _parâmetro lpProgress_ é ignorado, a menos que o sinalizador MESSAGE_DIALOG seja definido em  _ulFlags_.
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla como a operação de cópia ou movimentação é realizada. Os sinalizadores a seguir podem ser definidos:
    
MESSAGE_DIALOG 
  
> Solicita a exibição de um indicador de progresso.
    
MESSAGE_MOVE 
  
> As mensagens devem ser movidas, em vez de copiadas. Se MESSAGE_MOVE não estiver definida, as mensagens serão copiadas.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A operação de cópia ou movimentação foi bem-sucedida.
    
MAPI_E_USER_CANCEL 
  
> O usuário cancelou a operação, normalmente clicando no botão Cancelar **em** uma caixa de diálogo. 
    
## <a name="remarks"></a>Comentários

O **método IMAPISupport::CopyMessages** é implementado para objetos de suporte do provedor de armazenamento de mensagens. Os provedores de armazenamento de mensagens podem chamar **IMAPISupport::CopyMessages** na implementação de [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) para copiar ou mover uma ou mais mensagens de uma pasta para outra. Como parte da chamada **IMAPISupport::CopyMessages,** o provedor de armazenamento de mensagens pode especificar que MAPI deve exibir um indicador de progresso. 
  
## <a name="see-also"></a>Confira também



[IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

