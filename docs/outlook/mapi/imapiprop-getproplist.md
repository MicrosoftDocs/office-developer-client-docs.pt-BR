---
title: IMAPIPropGetPropList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetPropList
api_type:
- COM
ms.assetid: 0069c223-32bb-4286-b763-39fd45dc263b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5417853dbb1fa87d2beead2f73ca57329e17b044
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571119"
---
# <a name="imapipropgetproplist"></a>IMAPIProp::GetPropList

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna as marcas de propriedade para todas as propriedades. 
  
```cpp
HRESULT GetPropList(
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTagArray
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla o formato de cadeias de caracteres nas marcas de propriedade retornados. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres retornadas estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.
    
 _lppPropTagArray_
  
> [out] Um ponteiro para um ponteiro para a matriz de marca de propriedade que contém marcas para todas as propriedades do objeto.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> Todas as marcas de propriedade foram retornadas com êxito.
    
MAPI_E_BAD_CHARWIDTH 
  
> Tanto o sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode, ou MAPI_UNICODE não foi definido e a implementação suporta somente Unicode.
    
## <a name="remarks"></a>Comentários

O método **IMAPIProp::GetPropList** recupera a marca de propriedade para cada propriedade suportada atualmente por um objeto. Se o objeto não oferece suporte atualmente todas as propriedades, **GetPropList** retorna uma matriz de marca de propriedade com o membro **cValues** definido como 0. 
  
O escopo das propriedades retornado pela **GetPropList** varia de provedor. Alguns provedores de serviços excluir essas propriedades para o qual o chamador não tem acesso. Todos os provedores de retornam as propriedades do tipo **PT_OBJECT**.
  
Se o objeto não oferece suporte a Unicode, **GetPropList** retorna MAPI_E_BAD_CHARWIDTH, mesmo se não houver nenhuma propriedade de cadeia de caracteres definida para o objeto. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Provedores de transporte remoto implementam **GetPropList** exatamente conforme especificado aqui. Não há nenhuma preocupações especiais. A implementação deve, obviamente, retornar a mesma lista de propriedades como suportados pelo método [IMAPIProp::GetProps](imapiprop-getprops.md) . 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Chame a função [MAPIFreeBuffer](mapifreebuffer.md) para liberar a matriz de marca de propriedade apontada pela _lppPropTagArray_. 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetPropsNULL  <br/> |MFCMAPI usa o método **IMAPIProp::GetPropList** para obter uma lista de propriedades a serem passados para **GetProps**.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

