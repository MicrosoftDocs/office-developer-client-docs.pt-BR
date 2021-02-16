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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 7351457dc5b72cfc4a7ef9f91e9d33a80ca98c39
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414064"
---
# <a name="imapitablesetcollapsestate"></a>IMAPITable::SetCollapseState

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Recria o estado expandido ou recolhido atual de uma tabela categorizada usando dados salvos por uma chamada anterior para o método [IMAPITable::GetCollapseState.](imapitable-getcollapsestate.md) 
  
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
  
> [in] Contagem de bytes na estrutura apontada pelo parâmetro _pbCollapseState._ 
    
 _pbCollapseState_
  
> [in] Ponteiro para as estruturas que contêm os dados necessários para recriar o ponto de vista da tabela.
    
 _lpbkLocation_
  
> [out] Ponteiro para um indicador que identifica a linha na tabela na qual o estado recolhido ou expandido deve ser reconstruído. Esse indicador e a chave de instância passadas no parâmetro  _lpbInstanceKey_ na chamada para [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) identificam a mesma linha. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O estado da tabela categorizada foi reconstruído com êxito.
    
MAPI_E_BUSY 
  
> Outra operação está em andamento que impede o início da operação. A operação em andamento deve ter permissão para ser concluída ou deve ser interrompida.
    
MAPI_E_UNABLE_TO_COMPLETE 
  
> A tabela não pôde concluir a recomposição do ponto de vista recolhido ou expandido.
    
## <a name="remarks"></a>Comentários

O **método IMAPITable::SetCollapseState** restabelece o estado expandido ou recolhido do modo de exibição de tabela. **SetCollapseState** e **GetCollapseState** funcionam juntos da seguinte forma: 
  
1. Quando o estado de uma tabela categorizada está prestes a mudar, [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) é chamado para salvar todos os dados pertencentes ao estado antes da alteração. 
    
2. Para restaurar o modo de exibição da tabela ao seu estado salvo, **SetCollapseState** é chamado. Os dados salvos por **GetCollapseState** são passados para **SetCollapseState**. **SetCollapseState** é capaz de usar esses dados para restaurar o estado. 
    
3. **SetCollapseState** retorna como um parâmetro de saída um indicador que identifica a mesma linha que a chave de instância passada como entrada para **GetCollapseState**.
    
Para obter mais informações sobre tabelas categorizadas, consulte [Classificação e Categorização.](sorting-and-categorization.md) 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Você é responsável por verificar se a ordem de classificação e as restrições são exatamente as mesmas que eram no momento da chamada **GetCollapseState.** Se uma alteração tiver sido feita, **SetCollapseState** não deverá ser chamado porque os resultados podem ser imprevisíveis. Isso pode acontecer se, por exemplo, um cliente chamar **GetCollapseState** e, em seguida, **SortTable** alterar a chave de classificação antes de chamar **SetCollapseState**. Para garantir a segurança, verifique se os dados salvos ainda são válidos antes de prosseguir com a restauração. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para chamar **SetCollapseState,** você deve ter chamado **GetCollapseState anteriormente.** A ordem de classificação que estabelece as categorias deve ser a mesma para ambos os métodos. Se as ordens de classificação são diferentes, os resultados da **operação SetCollapseState** são imprevisíveis. 
  
## <a name="see-also"></a>Confira também



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

