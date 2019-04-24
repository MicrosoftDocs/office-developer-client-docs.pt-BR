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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328830"
---
# <a name="imapitablesetcollapsestate"></a>IMAPITable::SetCollapseState

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Recria o estado atual expandido ou recolhido de uma tabela categorizada usando dados que foram salvos por uma chamada anterior para o método [IMAPITable::](imapitable-getcollapsestate.md) getcollapsestate. 
  
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
  
> Serve deve ser zero.
    
 _cbCollapseState_
  
> no Contagem de bytes na estrutura apontada pelo parâmetro _pbCollapseState_ . 
    
 _pbCollapseState_
  
> no Ponteiro para as estruturas que contêm os dados necessários para reconstruir o modo de exibição de tabela.
    
 _lpbkLocation_
  
> bota Ponteiro para um indicador identificando a linha na tabela na qual o estado recolhido ou expandido deve ser recriado. Este indicador e a chave de instância passada no parâmetro _lpbInstanceKey_ na chamada para IMAPITable [::](imapitable-getcollapsestate.md) getcollapsestate identificam a mesma linha. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O estado da tabela categorizada foi reconstruído com êxito.
    
MAPI_E_BUSY 
  
> Outra operação está em andamento, o que impede a inicialização da operação. A operação em andamento deve ter permissão para ser concluída ou deve ser interrompida.
    
MAPI_E_UNABLE_TO_COMPLETE 
  
> A tabela não pôde concluir a reconstrução da exibição recolhida ou expandida.
    
## <a name="remarks"></a>Comentários

O método imApitable **::** setcollapsestate restabelece o estado expandido ou recolhido do modo de exibição de tabela. **** Setcollapsestate e **** getcollapsestate funcionam juntos da seguinte maneira: 
  
1. Quando o estado de uma tabela categorizada está prestes a mudar, [IMAPITable::](imapitable-getcollapsestate.md) getcollapsestate é chamado para salvar todos os dados pertencentes ao estado anterior à alteração. 
    
2. Para restaurar o modo de exibição da tabela para seu estado salvo **** , setcollapsestate é chamado. Os dados salvos por **** getcollapsestate são passados para **** setcollapsestate. **** Setcollapsestate é capaz de usar esses dados para restaurar o estado. 
    
3. **** Setcollapsestate retorna como um parâmetro de saída um indicador que identifica a mesma linha que a chave de instância passada como entrada para getcollapsestate. ****
    
Para obter mais informações sobre tabelas categorizadas, consulte [classificação e categorização](sorting-and-categorization.md). 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Você é responsável por verificar se a ordem de classificação e as restrições são exatamente iguais às que foram no momento da chamada getCollapsestate. **** Se uma alteração tiver sido feita, **** setcollapsestate não deverá ser chamado porque os resultados podem ser imprevisíveis. Isso pode acontecer se, por exemplo, um cliente chama **** getcollapsestate e **SortTable** para alterar a chave de classificação antes de **** chamar setcollapsestate. Para ser seguro, verifique se os dados salvos ainda são válidos antes de prosseguir com a restauração. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para chamar **** setcollapsestate, você deve ter chamado getcollapsestate anteriormente. **** A ordem de classificação que estabelece as categorias deve ser a mesma para os dois métodos. Se as ordens de classificação forem diferentes, os resultados **** da operação setcollapsestate serão imprevisíveis. 
  
## <a name="see-also"></a>Confira também



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

