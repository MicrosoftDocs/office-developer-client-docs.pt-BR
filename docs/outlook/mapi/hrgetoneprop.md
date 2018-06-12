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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 4dcdce72781669988a0cb15eb9b3a7cd73494bfb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766807"
---
# <a name="hrgetoneprop"></a>HrGetOneProp

  
  
**Aplica-se a**: Outlook 
  
Recupera o valor de uma única propriedade de uma interface de propriedade, ou seja, uma interface derivada [IMAPIProp](imapipropiunknown.md). 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
HrGetOneProp(
  LPMAPIPROP pmp,
  ULONG ulPropTag,
  LPSPropValue FAR * ppprop
);
```

## <a name="parameters"></a>Par�metros

 _PMP_
  
> [in] Ponteiro para a interface de [IMAPIProp](imapipropiunknown.md) do qual o valor da propriedade deve ser recuperado. 
    
 _ulPropTag_
  
> [in] Marca de propriedade da propriedade a ser recuperado. 
    
 _ppprop_
  
> [out] Ponteiro para um ponteiro para a estrutura [SPropValue](spropvalue.md) retornada, definindo o valor da propriedade recuperadas. 
    
## <a name="return-value"></a>Valor retornado

E_NOT_FOUND 
  
> A propriedade solicitada não está disponível da interface especificada.
    
## <a name="remarks"></a>Coment�rios

Ao contrário do método [IMAPIProp::GetProps](imapiprop-getprops.md) , a função **HrGetOneProp** nunca retorna qualquer aviso. Porque ele recupera apenas uma propriedade, ele simplesmente for bem-sucedido ou falha. Para recuperar as várias propriedades, **GetProps** é mais rápido. 
  
Você pode definir ou alterar uma única propriedade com a função [HrSetOneProp](hrsetoneprop.md) . 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetMAPIObjectType  <br/> |MFCMAPI usa o método **HrGetOneProp** para recuperar o tipo de um objeto.  <br/> |
   
## <a name="see-also"></a>Confira também



[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

