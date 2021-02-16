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
  
Recupera atributos de propriedades em um [objeto IMessage](imessageimapiprop.md) fornecido pela [função OpenIMsgOnIStg.](openimsgonistg.md) 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Imessage.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de armazenamento de mensagens  <br/> |
   
```cpp
HRESULT GetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTagArray,
  LPSPropAttrArray FAR * lppPropAttrArray
);
```

## <a name="parameters"></a>Parâmetros

 _lpObject_
  
> [in] Ponteiro para um **objeto IMessage** obtido da [função OpenIMsgOnIStg.](openimsgonistg.md) 
    
 _lpPropTagArray_
  
> [in] Ponteiro para uma [estrutura SPropTagArray](sproptagarray.md) que contém uma matriz de marcas de propriedade indicando as propriedades para as quais os atributos devem ser recuperados. 
    
 _lppPropAttrArray_
  
> [out] Ponteiro para um ponteiro para a [estrutura SPropAttrArray](spropattrarray.md) retornada que contém os atributos de propriedade recuperados. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados. 
    
MAPI_W_ERRORS_RETURNED 
  
> A chamada foi bem-sucedida em geral, mas uma ou mais propriedades não puderam ser acessadas e foram retornadas com um tipo de propriedade de PT_ERROR.
    
## <a name="remarks"></a>Comentários

Atributos de propriedade só podem ser acessados em objetos de propriedade, ou seja, objetos que implementam o [IMAPIProp : interface IUnknown.](imapipropiunknown.md) Para disponibilizar propriedades MAPI em um objeto de armazenamento estruturado OLE, [OpenIMsgOnIStg](openimsgonistg.md) cria um [IMessage : objeto IMAPIProp](imessageimapiprop.md) sobre o objeto **IStorage** OLE. Os atributos de propriedade nesses objetos podem ser definidos ou alterados com [SetAttribIMsgOnIStg](setattribimsgonistg.md) e recuperados com **GetAttribIMsgOnIStg**. 
  
> [!NOTE]
> **GetAttribIMsgOnIStg** e **SetAttribIMsgOnIStg** não operam em todos os **objetos IMessage.** Eles só são **válidos para objetos IMessage**-on-IStorage retornados por **OpenIMsgOnIStg**.  
  
O número e as posições dos atributos no parâmetro _lppPropAttrArray_ correspondem ao número e às posições das marcas de propriedade no parâmetro _lpPropTagArray._ 
  

