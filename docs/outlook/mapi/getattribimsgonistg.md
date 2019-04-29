---
title: GetAttribIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.GetAttribIMsgOnIStg
api_type:
- COM
ms.assetid: bb27b28a-b2bd-4d4a-b0bb-0692f3de8e16
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 16e85eabc067bd82f5fb89c917afaf2831c75673
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439993"
---
# <a name="getattribimsgonistg"></a>GetAttribIMsgOnIStg

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Recupera atributos de propriedades em um objeto [IMessage](imessageimapiprop.md) fornecido pela função [OpenIMsgOnIStg](openimsgonistg.md) . 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |IMessage. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Provedores de repositórios de mensagens e aplicativos cliente  <br/> |
   
```cpp
HRESULT GetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTagArray,
  LPSPropAttrArray FAR * lppPropAttrArray
);
```

## <a name="parameters"></a>Parâmetros

 _lpObject_
  
> no Ponteiro para um objeto **IMessage** obtido da função [OpenIMsgOnIStg](openimsgonistg.md) . 
    
 _lpPropTagArray_
  
> no Ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) que contém uma matriz de marcas de propriedade indicando as propriedades para as quais os atributos devem ser recuperados. 
    
 _lppPropAttrArray_
  
> bota Ponteiro para um ponteiro para a estrutura [SPropAttrArray](spropattrarray.md) retornada que contém os atributos de propriedade recuperados. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados. 
    
MAPI_W_ERRORS_RETURNED 
  
> A chamada foi bem-sucedida, mas uma ou mais propriedades não puderam ser acessadas e retornadas com um tipo de propriedade de PT_ERROR.
    
## <a name="remarks"></a>Comentários

Atributos de propriedade só podem ser acessados em objetos Property, ou seja, objetos que implementam a interface [IMAPIProp: IUnknown](imapipropiunknown.md) . Para disponibilizar as propriedades MAPI em um objeto de armazenamento estruturado OLE, [OpenIMsgOnIStg](openimsgonistg.md) cria um objeto [IMessage: IMAPIProp](imessageimapiprop.md) na parte superior do objeto OLE **IStorage** . Os atributos de propriedade desses objetos podem ser definidos ou alterados com [SetAttribIMsgOnIStg](setattribimsgonistg.md) e recuperados com o **GetAttribIMsgOnIStg**. 
  
> [!NOTE]
> **GetAttribIMsgOnIStg** e **SetAttribIMsgOnIStg** não operam em todos os objetos **IMessage** . Eles são válidos apenas para objetos **IMessage**-on- **IStorage** retornados por **OpenIMsgOnIStg**. 
  
O número e as posições dos atributos no parâmetro _lppPropAttrArray_ correspondem ao número e às posições das marcas de propriedade no parâmetro _lpPropTagArray_ . 
  

