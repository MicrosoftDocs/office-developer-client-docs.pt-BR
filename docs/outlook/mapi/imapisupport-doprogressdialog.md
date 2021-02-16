---
title: IMAPISupportDoProgressDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoProgressDialog
api_type:
- COM
ms.assetid: 74c52b96-e903-444b-8bda-73a08f278c22
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 3de29e9af5caa82d2e57c8fcbbdab7d5ddb19dd9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432580"
---
# <a name="imapisupportdoprogressdialog"></a>IMAPISupport::DoProgressDialog

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Recupera um objeto de progresso que exibe um indicador de progresso.
  
```cpp
HRESULT DoProgressDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIPROGRESS FAR * lppProgress
);
```

## <a name="parameters"></a>Parâmetros

 _ulUIParam_
  
> [in] Um alça para a janela pai do indicador de progresso.
    
 _ulFlags_
  
> [in] Uma bitmask de sinalizadores que controla como o objeto de progresso deve calcular o progresso. O sinalizador a seguir pode ser definido:
    
MAPI_TOP_LEVEL 
  
> O andamento é calculado para um item de nível superior, como uma pasta pai. O objeto de progresso deve usar os valores nos parâmetros _ulCount_ e _ulTotal_ do método [IMAPIProgress::P ess](imapiprogress-progress.md) — que indicam o item atual e o total de itens na operação, respectivamente — para incrementar o indicador de progresso da operação. 
    
 _lppProgress_
  
> [out] Um ponteiro para um ponteiro para o objeto de progresso.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O objeto de progresso foi recuperado com êxito.
    
## <a name="remarks"></a>Comentários

O **método IMAPISupport::D oProgressDialog** é implementado para objetos de suporte de provedor de armazenamento de endereços e de armazenamento de mensagens. Esses provedores chamam **DoProgressDialog** para acessar a implementação de MAPI da interface [IMAPIProgress,](imapiprogressiunknown.md) que calcula as informações de progresso e exibe uma caixa de diálogo padrão. 
  
Para obter informações sobre como usar um objeto de progresso e a interface **IMAPIProgress,** consulte [Exibir um indicador de progresso.](how-to-display-a-progress-indicator.md)
  
## <a name="see-also"></a>Confira também



[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[Exibir um indicador de progresso](how-to-display-a-progress-indicator.md)

