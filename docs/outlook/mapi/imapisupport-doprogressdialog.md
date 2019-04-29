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
  
Recupera um objeto Progress que exibe um indicador de progresso.
  
```cpp
HRESULT DoProgressDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIPROGRESS FAR * lppProgress
);
```

## <a name="parameters"></a>Parâmetros

 _ulUIParam_
  
> no Uma alça para a janela pai do indicador de progresso.
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla como o objeto Progress deve calcular o andamento. O seguinte sinalizador pode ser definido:
    
MAPI_TOP_LEVEL 
  
> O andamento é calculado para um item de nível superior, como uma pasta pai. O objeto Progress deve usar os valores no [método imapiprogress::P rogress](imapiprogress-progress.md) do método _ulCount_ e _ulTotal_ parâmetros, que indicam o item atual e o total de itens na operação, respectivamente, para incrementar o progresso indicador para a operação. 
    
 _lppProgress_
  
> bota Um ponteiro para um ponteiro para o objeto Progress.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O objeto Progress foi recuperado com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport::D oprogressdialog** é implementado para os objetos de suporte para o catálogo de endereços e o provedor de repositório de mensagens. Esses provedores chamam o **DoProgressDialog** para acessar a implementação de MAPI da interface [método imapiprogress](imapiprogressiunknown.md) , que calcula as informações de progresso e exibe uma caixa de diálogo padrão. 
  
Para obter informações sobre como usar um objeto Progress e a interface **método imapiprogress** , consulte [exibir um indicador de progresso](how-to-display-a-progress-indicator.md).
  
## <a name="see-also"></a>Confira também



[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[Exibir um indicador de progresso](how-to-display-a-progress-indicator.md)

