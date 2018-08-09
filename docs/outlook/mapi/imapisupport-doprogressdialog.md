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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 527a7bb3201a4a6b1bc0807136bc88b80c189de2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767244"
---
# <a name="imapisupportdoprogressdialog"></a>IMAPISupport::DoProgressDialog

  
  
**Aplica-se a**: Outlook 
  
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
  
> [in] Um identificador para a janela pai do indicador de progresso.
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como o objeto de progresso deve calcular o progresso. O seguinte sinalizador pode ser definido:
    
MAPI_TOP_LEVEL 
  
> Progresso é calculado para um item de nível superior, como uma pasta pai. O objeto de progresso deve usar os valores nos parâmetros do método [IMAPIProgress::Progress](imapiprogress-progress.md) de _ulCount_ e _ulTotal_ — que indicam o item atual e o total de itens na operação, respectivamente — para incrementar o progresso indicador para a operação. 
    
 _lppProgress_
  
> [out] Um ponteiro para um ponteiro para o objeto de andamento.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O objeto de andamento foi recuperado com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport::DoProgressDialog** é implementado para endereço livro e mensagem provedor suporte objetos store. Esses provedores chamarem **DoProgressDialog** para acessar a implementação de MAPI da interface [IMAPIProgress](imapiprogressiunknown.md) , que calcula as informações de andamento e exibe uma caixa de diálogo padrão. 
  
Para obter informações sobre como usar um objeto de progresso e a interface de **IMAPIProgress** , consulte [Exibir um indicador de progresso](how-to-display-a-progress-indicator.md).
  
## <a name="see-also"></a>Confira também



[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[Exibir um indicador de progresso](how-to-display-a-progress-indicator.md)

