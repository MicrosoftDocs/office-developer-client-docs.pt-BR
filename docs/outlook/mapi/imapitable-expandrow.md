---
title: IMAPITableExpandRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.ExpandRow
api_type:
- COM
ms.assetid: b96dd8f6-e648-4014-8a1d-ae1da771c439
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 1b3d8c74d85696e733b378a4cac2b8e2a3b6a072
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767315"
---
# <a name="imapitableexpandrow"></a>IMAPITable::ExpandRow

  
  
**Aplica-se a**: Outlook 
  
Expande uma categoria de tabela recolhida, adicionando a folha ou linhas de cabeçalho de nível inferior que pertencem à categoria para o modo de exibição de tabela.
  
```cpp
HRESULT ExpandRow(
ULONG cbInstanceKey,
LPBYTE pbInstanceKey,
ULONG ulRowCount,
ULONG ulFlags,
LPSRowSet FAR * lppRows,
ULONG FAR * lpulMoreRows
);
```

## <a name="parameters"></a>Par�metros

 _cbInstanceKey_
  
> [in] A contagem de bytes na propriedade PR_INSTANCE_KEY apontado pelo parâmetro _pbInstanceKey_ . 
    
 _pbInstanceKey_
  
> [in] Um ponteiro para a propriedade **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) que identifica a linha de título para a categoria. 
    
 _ulRowCount_
  
> [in] O número máximo de linhas a serem retornadas no parâmetro _lppRows_ . 
    
 _ulFlags_
  
> Reservado; deve ser zero.
    
 _lppRows_
  
> [out] Um ponteiro para uma estrutura [SRowSet](srowset.md) recebendo as linhas primeira (até _ulRowCount_) que foram inseridas em um modo de exibição de tabela como resultado da expansão. Essas linhas são inseridas após a linha de título identificada pelo parâmetro _pbInstanceKey_ . O parâmetro _lppRows_ pode ser NULL se o parâmetro _ulRowCount_ for zero. 
    
 _lpulMoreRows_
  
> [out] Um ponteiro para o número total de linhas que foram adicionados ao modo de exibição de tabela.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A categoria foi expandida com êxito.
    
E_NOT_FOUND 
  
> A linha identificada pelo parâmetro _pbInstanceKey_ não existe. 
    
## <a name="remarks"></a>Coment�rios

O método **IMAPITable::ExpandRow** expande uma categoria de tabela recolhida, adicionando a folha ou linhas de cabeçalho de nível inferior que pertencem à categoria para o modo de exibição de tabela. Um limite no número de linhas a serem retornados no parâmetro _lppRows_ pode ser especificado no parâmetro _ulRowCount_ . Quando _ulRowCount_ estiver definida como um valor maior que zero e uma ou mais linhas são retornadas no conjunto de linha apontado pela _lppRows_, defina a posição do indicador que bookmark_current é movido para a linha imediatamente após a última linha a linha.
  
Quando _ulRowCount_ estiver definida como zero, solicitando que zero folha ou linhas de título de nível inferior adicionadas à categoria ou zero linhas são retornadas porque não há nenhuma folha ou linhas de cabeçalho de nível inferior na categoria, a posição do BOOKMARK_CURRENT é definida como a linha seguindo a linha identificada pela _pbInstanceKey_. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Sem gere notificações em linhas que são adicionadas a um modo de exibição de tabela devido à expansão de categoria.
  
## <a name="notes-to-callers"></a>Notas para chamadores

O número de linhas no conjunto de linha apontado pelo parâmetro _lppRows_ não pode ser igual ao número de linhas que realmente foram adicionados à tabela, todo o conjunto de folha ou heading linhas para a categoria de nível inferior. Podem ocorrer erros, como memória insuficiente ou o número de linhas na categoria exceder o número especificado no parâmetro _ulRowCount_ . Em ambos os casos, BOOKMARK_CURRENT será posicionada na última linha retornada. Para recuperar imediatamente o restante das linhas da categoria, chame [IMAPITable:: QueryRows](imapitable-queryrows.md).
  
Não espera receber uma notificação de tabela quando seu estado de mudar de uma categoria. Você pode manter um cache local de linhas que podem ser atualizados com cada chamada **ExpandRow** ou **CollapseRow** . 
  
Para obter mais informações sobre tabelas categorizadas, consulte [classificação e categorização](sorting-and-categorization.md).
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::DoExpandCollapse  <br/> |MFCMAPI usa o método **IMAPITable::ExpandRow** para expandir uma categoria de tabela recolhida.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPITable::CollapseRow](imapitable-collapserow.md)
  
[IMAPITable: IUnknown](imapitableiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

