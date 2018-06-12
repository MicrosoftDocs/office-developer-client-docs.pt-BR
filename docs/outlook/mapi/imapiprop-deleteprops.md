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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 8eb19f9a2d3458e153b0758b56c502ce612be0cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767159"
---
# <a name="imapipropdeleteprops"></a>IMAPIProp::DeleteProps

  
  
**Aplica-se a**: Outlook 
  
Exclui uma ou mais propriedades de um objeto. 
  
```cpp
HRESULT DeleteProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Par�metros

 _lpPropTagArray_
  
> [in] Um ponteiro para uma matriz de marcas de propriedade que indicam as propriedades a ser excluído. O membro **cValues** da estrutura [SPropTagArray](sproptagarray.md) apontado pela _lpPropTagArray_ não deve ser zero e o parâmetro _lpPropTagArray_ em si não deve ser NULL. 
    
 _lppProblems_
  
> [além, out] Na entrada, um ponteiro para um ponteiro para uma estrutura [SPropProblemArray](spropproblemarray.md) ; Caso contrário, NULL, que indica que não há nenhuma necessidade de informações de erro. Se _lppProblems_ for um ponteiro válido na entrada, **DeleteProps** retorna informações detalhadas sobre erros ao excluir uma ou mais propriedades. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> Propriedades foram excluídas com êxito.
    
MAPI_E_NO_ACCESS 
  
> O chamador não tem permissões suficientes para excluir as propriedades.
    
## <a name="remarks"></a>Coment�rios

O método **IMAPIProp::DeleteProps** remove uma ou mais propriedades do objeto atual. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Você não precisará permitir propriedades a ser excluído de todos os objetos. Se o objeto não é modificável, retorne MAPI_E_NO_ACCESS do método **DeleteProps** . 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Você não precisará definir o tipo de propriedade para cada marca de propriedade da matriz de marca de propriedade apontado pelo parâmetro _lpPropTagArray_ . Tipos de propriedade serão ignorados; somente os identificadores de propriedade são usados. 
  
Lembre-se de que alguns objetos não permita modificação e que esses objetos retornam MAPI_E_NO_ACCESS do método **DeleteProps** . Permitir que outros objetos, algumas propriedades a ser excluído, mas não para outras. Quando há um problema ao excluir apenas algumas das propriedades, **DeleteProps** Retorna S_OK. Se você tiver passado um ponteiro válido no parâmetro _lppProblems_ , **DeleteProps** definirá o ponteiro em uma estrutura de **SPropProblemArray** que contém informações detalhadas sobre os problemas com cada propriedade. Por exemplo, se você estiver excluindo todas as propriedades de uma mensagem e há um problema com um ou mais dos seus respectivos anexos, a estrutura de **SPropProblemArray** irá conter uma entrada para o **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments ](pidtagmessageattachments-canonical-property.md)) propriedade. 
  
A estrutura apontada pela _lppProblems_ só será válida se **DeleteProps** Retorna S_OK. Se **DeleteProps** retornará um erro, não tente usar a estrutura **SPropProblemArray** . Em vez disso, chame o método do objeto [IMAPIProp::GetLastError](imapiprop-getlasterror.md) para obter mais informações sobre o erro. 
  
Libere a estrutura de **SPropProblemArray** retornada ao chamar a função [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |DeleteProperty  <br/> |MFCMAPI usa o método **IMAPIProp::DeleteProps** para excluir uma propriedade de um objeto.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp: IUnknown](imapipropiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

