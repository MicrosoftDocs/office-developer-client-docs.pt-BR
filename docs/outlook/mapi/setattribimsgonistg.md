---
title: SetAttribIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SetAttribIMsgOnIStg
api_type:
- COM
ms.assetid: 683d0d00-1b93-445d-86ff-180a3e6d2323
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e8a0daa2afe2397f39b7f37a31ef718ba65a3350
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770382"
---
# <a name="setattribimsgonistg"></a>SetAttribIMsgOnIStg

  
  
**Aplica-se a**: Outlook 
  
Define ou altera atributos das propriedades em um objeto [IMessage](imessageimapiprop.md) fornecido pela função [OpenIMsgOnIStg](openimsgonistg.md) . 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |IMessage.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de armazenamento de mensagens e aplicativos cliente  <br/> |
   
```cpp
HRESULT SetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTags,
  LPSPropAttrArray lpPropAttrs,
  LPSPropProblemArray FAR * lppPropProblems
);
```

## <a name="parameters"></a>Parâmetros

 _lpObject_
  
> [in] Ponteiro para o objeto para o qual propriedade atributos estão sendo definidos. 
    
 _lpPropTags_
  
> [in] Ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) contendo uma matriz das marcas de propriedade indicando as propriedades para o qual propriedade atributos estão sendo definidos. 
    
 _lpPropAttrs_
  
> [in] Ponteiro para uma estrutura [SPropAttrArray](spropattrarray.md) listando os atributos de propriedade para definir. 
    
 _lppPropProblems_
  
> [out] Ponteiro para a estrutura de [SPropProblemArray](spropproblemarray.md) retornado contendo um conjunto de problemas de propriedade. Essa estrutura identifica os problemas encontrados se **SetAttribIMsgOnIStg** tiver sido apto a definir algumas propriedades, mas não todos. Se o parâmetro _lppPropProblems_ é passado um ponteiro como NULL, nenhuma matriz de problema de propriedade é retornado, mesmo se algumas propriedades não foram definidas. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
MAPI_W_ERRORS_RETURNED 
  
> Chamada bem-sucedida, mas uma ou mais propriedades não pôde ser acessadas e foram retornadas com um tipo de propriedade de PT_ERROR.
    
## <a name="remarks"></a>Comentários

Atributos de propriedade só podem ser acessados na propriedade objetos, ou seja, objetos Implementando o [IMAPIProp: IUnknown](imapipropiunknown.md) interface. Para disponibilizar propriedades MAPI em um objeto de armazenamento estruturado OLE, [OpenIMsgOnIStg](openimsgonistg.md) cria um [IMessage: IMAPIProp](imessageimapiprop.md) objeto na parte superior do objeto OLE **IStorage** . Os atributos de propriedade nesses objetos podem ser definidos ou alterados com **SetAttribIMsgOnIStg** e recuperados com [GetAttribIMsgOnIStg](getattribimsgonistg.md). 
  
 **Observação** **GetAttribIMsgOnIStg** e **SetAttribIMsgOnIStg** não operam em todos os objetos **IMessage** . Eles só são válidos para **IMessage**- on - objetos **IStorage** retornados por **OpenIMsgOnIStg**. 
  
O parâmetro _lpPropAttrs_ , o número e a posição dos atributos devem coincidir com o número e a posição das marcas de propriedade passado no parâmetro _lpPropTags_ . 
  
A função **SetAttribIMsgOnIStg** é usada para tornar as propriedades da mensagem somente leitura quando exigido pelo esquema **IMessage** . O provedor de armazenamento de mensagem de amostra usa-lo para essa finalidade. Para obter mais informações, consulte [Messages](mapi-messages.md). 
  

