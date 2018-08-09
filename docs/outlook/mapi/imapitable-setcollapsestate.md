---
title: IMAPITableSetCollapseState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SetCollapseState
api_type:
- COM
ms.assetid: 31325e8f-1cf9-49b2-8118-953996b0037f
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 252b6d6c7ff74acd5f0b288af48ff2901c2330ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767356"
---
# <a name="imapitablesetcollapsestate"></a>IMAPITable::SetCollapseState

  
  
**Aplica-se a**: Outlook 
  
Recriará o estado atual de expandidos ou recolhido de uma tabela categorizado usando os dados que foi salvo por uma chamada anterior para o método [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) . 
  
```cpp
HRESULT SetCollapseState(
ULONG ulFlags,
ULONG cbCollapseState,
LPBYTE pbCollapseState,
BOOKMARK FAR * lpbkLocation
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> Reservado; deve ser zero.
    
 _cbCollapseState_
  
> [in] Contagem de bytes na estrutura apontado pelo parâmetro _pbCollapseState_ . 
    
 _pbCollapseState_
  
> [in] Ponteiro para as estruturas contendo os dados necessários para recriar o modo de exibição de tabela.
    
 _lpbkLocation_
  
> [out] Ponteiro para um indicador que identifica a linha da tabela na qual o estado recolhido ou expandido deve ser recriado. Este indicador e a chave de instância passada no parâmetro _lpbInstanceKey_ na chamada a [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) identificam a mesma linha. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O estado da tabela categorizado foi reconstruído com êxito.
    
MAPI_E_BUSY 
  
> Outra operação está em andamento que impede que a operação seja iniciado. Ou a operação em andamento deve ter permissão para concluir ou ele deve ser interrompido.
    
MAPI_E_UNABLE_TO_COMPLETE 
  
> A tabela não pôde concluir a recriação o modo de exibição recolhido ou expandido.
    
## <a name="remarks"></a>Comentários

O método **IMAPITable::SetCollapseState** restabelece o estado expandido ou recolhido do modo de exibição de tabela. **SetCollapseState** e **GetCollapseState** funcionam juntas da seguinte maneira: 
  
1. Quando o estado de uma tabela categorizado está prestes a ser alterada, [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) é chamado para salvar todos os dados referentes ao estado anterior a alteração. 
    
2. Para restaurar o modo de exibição da tabela ao seu estado salvo, **SetCollapseState** é chamado. Os dados salvos pelo **GetCollapseState** são passados para **SetCollapseState**. **SetCollapseState** é capaz de usar esses dados para restaurar o estado. 
    
3. **SetCollapseState** retorna um indicador que identifica a mesma linha como a chave de instância passada como entrada para **GetCollapseState**como um parâmetro de saída.
    
Para obter mais informações sobre tabelas categorizadas, consulte [classificação e categorização](sorting-and-categorization.md). 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Você é responsável por verificar que a ordem de classificação e restrições forem exatamente iguais como estavam no momento da chamada **GetCollapseState** . Se uma alteração foi feita, **SetCollapseState** não deve ser chamado porque os resultados podem ser imprevisíveis. Isso pode acontecer se, por exemplo, um cliente chama **GetCollapseState** e **SortTable** para alterar a chave de classificação antes de chamar **SetCollapseState**. Para estar seguro, verifique se os dados salvos ainda são válidos antes de prosseguir com a restauração. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para chamar **SetCollapseState**, você anteriormente deve ter chamado **GetCollapseState**. A ordem de classificação estabelecer as categorias deve ser o mesmo para os dois métodos. Se as ordens de classificação forem diferentes, os resultados da operação **SetCollapseState** serão imprevisíveis. 
  
## <a name="see-also"></a>Confira também



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

