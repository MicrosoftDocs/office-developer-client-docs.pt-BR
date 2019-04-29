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
ms.openlocfilehash: f089fa2c608fb9fcb7deba2e061c5cf5886aa02f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414785"
---
# <a name="imapipropgetproplist"></a>IMAPIProp::GetPropList

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna as marcas de propriedade de todas as propriedades. 
  
```cpp
HRESULT GetPropList(
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTagArray
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla o formato das cadeias de caracteres nas marcas de propriedade retornadas. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres retornadas estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI.
    
 _lppPropTagArray_
  
> bota Um ponteiro para um ponteiro para a matriz de marca de propriedade que contém marcas para todas as propriedades do objeto.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> Todas as marcas de propriedade foram retornadas com êxito.
    
MAPI_E_BAD_CHARWIDTH 
  
> O sinalizador MAPI_UNICODE foi definido e a implementação não tem suporte para Unicode ou o MAPI_UNICODE não foi definido e a implementação oferece suporte somente a Unicode.
    
## <a name="remarks"></a>Comentários

O método **IMAPIProp::** getproplist recupera a marca de propriedade para cada propriedade atualmente aceita por um objeto. Se o objeto não suportar nenhuma propriedade no momento, **** getproplist retornará uma matriz de marca de propriedade com o membro **cValues** definido como 0. 
  
O escopo de propriedades retornado por **** getproplist varia de provedor para provedor. Alguns provedores de serviços excluem as propriedades para as quais o chamador não tem acesso. Todos os provedores retornam propriedades do tipo **PT_OBJECT**.
  
Se o objeto não oferecer suporte a Unicode **** , getproplist retornará MAPI_E_BAD_CHARWIDTH, mesmo se não houver propriedades de cadeia de caracteres definidas para o objeto. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Os provedores de transporte **** remotos implementam getproplist exatamente como especificado aqui. Não há preocupações especiais. A implementação deve, naturalmente, retornar a mesma lista de propriedades que é suportada pelo método [IMAPIProp::](imapiprop-getprops.md) GetProps. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Chame a função [MAPIFreeBuffer](mapifreebuffer.md) para liberar a matriz de marca de propriedade apontada por _lppPropTagArray_. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIFunctions. cpp  <br/> |GetPropsNULL  <br/> |MFCMAPI usa o método **IMAPIProp::** getproplist para obter uma lista de propriedades a ser **** passada para GetProps.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

