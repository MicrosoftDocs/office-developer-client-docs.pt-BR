---
title: IMAPIPropDeleteProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.DeleteProps
api_type:
- COM
ms.assetid: 5cc642de-21f0-4826-bf21-aac4bcfc1328
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5bfef87baa2dffa4605f9a7afa3833024f514430
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409234"
---
# <a name="imapipropdeleteprops"></a>IMAPIProp::DeleteProps

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Exclui uma ou mais propriedades de um objeto. 
  
```cpp
HRESULT DeleteProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Parâmetros

 _lpPropTagArray_
  
> [in] Um ponteiro para uma matriz de marcas de propriedade que indicam as propriedades a excluir. O **membro cValues** da estrutura [SPropTagArray](sproptagarray.md) apontado por  _lpPropTagArray_ não deve ser zero, e o próprio parâmetro  _lpPropTagArray_ não deve ser NULL. 
    
 _lppProblems_
  
> [in, out] Na entrada, um ponteiro para um ponteiro para uma [estrutura SPropProblemArray;](spropproblemarray.md) caso contrário, NULL, que indica que não há necessidade de informações de erro. Se  _lppProblems_ for um ponteiro válido na entrada, **DeleteProps** retornará informações detalhadas sobre erros ao excluir uma ou mais propriedades. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> As propriedades foram excluídas com êxito.
    
MAPI_E_NO_ACCESS 
  
> O chamador tem permissões insuficientes para excluir propriedades.
    
## <a name="remarks"></a>Comentários

O **método IMAPIProp::D eleteProps** remove uma ou mais propriedades do objeto atual. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Não é preciso permitir que as propriedades sejam excluídas de todos os objetos. Se o objeto não for modificável, retorne MAPI_E_NO_ACCESS do **método DeleteProps.** 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Você não precisa definir o tipo de propriedade para cada marca de propriedade na matriz de marca de propriedade apontado pelo parâmetro _lpPropTagArray._ Tipos de propriedade são ignorados; somente os identificadores de propriedade são usados. 
  
Esteja ciente de que alguns objetos não permitem modificação e que esses objetos retornam MAPI_E_NO_ACCESS do **método DeleteProps.** Outros objetos permitem que algumas propriedades sejam excluídas, mas não outras. Quando há um problema ao excluir apenas algumas das propriedades, **DeleteProps** retorna S_OK. Se você tiver passado um ponteiro válido no parâmetro  _lppProblems,_ **DeleteProps** definirá o ponteiro para uma estrutura **SPropProblemArray** que contém informações detalhadas sobre os problemas com cada propriedade. Por exemplo, se você estiver excluindo todas as propriedades de uma mensagem e houver um problema com um ou mais de seus anexos, a estrutura **SPropProblemArray** conterá uma entrada para a propriedade **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)). 
  
A estrutura apontada por  _lppProblems_ só será válida se **DeleteProps** retornar S_OK. Se **DeleteProps** retornar um erro, não tente usar a **estrutura SPropProblemArray.** Em vez disso, chame o método [IMAPIProp::GetLastError](imapiprop-getlasterror.md) do objeto para obter mais informações sobre o erro. 
  
Liberar a estrutura **SPropProblemArray** retornada chamando a [função MAPIFreeBuffer.](mapifreebuffer.md) 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |DeleteProperty  <br/> |MFCMAPI usa o **método IMAPIProp::D eleteProps** para excluir uma propriedade de um objeto.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

