---
title: HrGetOneProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrGetOneProp
api_type:
- HeaderDef
ms.assetid: 8d0a381a-e714-4663-9a57-b0e1cdbd6ba7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e5adc7d0c317d8b803645d78227777998d7d241f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416052"
---
# <a name="hrgetoneprop"></a>HrGetOneProp

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Recupera o valor de uma única propriedade de uma interface de propriedade, ou seja, uma interface derivada de [IMAPIProp](imapipropiunknown.md). 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
HrGetOneProp(
  LPMAPIPROP pmp,
  ULONG ulPropTag,
  LPSPropValue FAR * ppprop
);
```

## <a name="parameters"></a>Parâmetros

 _PMP_
  
> no Ponteiro para a interface [IMAPIProp](imapipropiunknown.md) da qual o valor da propriedade deve ser recuperado. 
    
 _ulPropTag_
  
> no Marca de propriedade da propriedade a ser recuperada. 
    
 _ppprop_
  
> bota Ponteiro para um ponteiro para a estrutura [SPropValue](spropvalue.md) retornada que define o valor da propriedade recuperado. 
    
## <a name="return-value"></a>Valor de retorno

MAPI_E_NOT_FOUND 
  
> A propriedade solicitada não está disponível na interface especificada.
    
## <a name="remarks"></a>Comentários

Diferentemente do método [IMAPIProp::](imapiprop-getprops.md) GetProps, a função **HrGetOneProp** nunca retorna qualquer aviso. Como ele recupera apenas uma propriedade, ele simplesmente Obtém ou falha. Para recuperar várias propriedades, getProps é mais rápido. **** 
  
Você pode definir ou alterar uma única propriedade com a função [HrSetOneProp](hrsetoneprop.md) . 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIFunctions. cpp  <br/> |GetMAPIObjectType  <br/> |MFCMAPI usa o método **HrGetOneProp** para recuperar o tipo de um objeto.  <br/> |
   
## <a name="see-also"></a>Confira também



[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

