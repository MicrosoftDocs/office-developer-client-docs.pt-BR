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
ms.openlocfilehash: 852ce31ba5ab02ff8f05dee25c9b32acb73130ec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337965"
---
# <a name="setattribimsgonistg"></a>SetAttribIMsgOnIStg

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define ou altera atributos de propriedades em um objeto [IMessage](imessageimapiprop.md) fornecido pela função [OpenIMsgOnIStg](openimsgonistg.md) . 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |IMessage. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Provedores de repositórios de mensagens e aplicativos cliente  <br/> |
   
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
  
> no Ponteiro para o objeto para o qual os atributos de propriedade estão sendo definidos. 
    
 _lpPropTags_
  
> no Ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) que contém uma matriz de marcas de propriedade indicando as propriedades para as quais os atributos de propriedade estão sendo definidos. 
    
 _lpPropAttrs_
  
> no Ponteiro para uma estrutura [SPropAttrArray](spropattrarray.md) listando os atributos de propriedade a serem definidos. 
    
 _lppPropProblems_
  
> bota Ponteiro para a estrutura [SPropProblemArray](spropproblemarray.md) retornada que contém um conjunto de problemas de propriedade. Esta estrutura identifica problemas encontrados se **SetAttribIMsgOnIStg** foi capaz de definir algumas propriedades, mas não todas. Se um ponteiro para NULL for passado no parâmetro _lppPropProblems_ , nenhuma matriz de problemas de propriedade será retornada, mesmo que algumas propriedades não tenham sido definidas. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
MAPI_W_ERRORS_RETURNED 
  
> A chamada foi bem-sucedida, mas uma ou mais propriedades não puderam ser acessadas e retornadas com um tipo de propriedade de PT_ERROR.
    
## <a name="remarks"></a>Comentários

Atributos de propriedade só podem ser acessados em objetos Property, ou seja, objetos que implementam a interface [IMAPIProp: IUnknown](imapipropiunknown.md) . Para disponibilizar as propriedades MAPI em um objeto de armazenamento estruturado OLE, [OpenIMsgOnIStg](openimsgonistg.md) cria um objeto [IMessage: IMAPIProp](imessageimapiprop.md) na parte superior do objeto OLE **IStorage** . Os atributos de propriedade desses objetos podem ser definidos ou alterados com **SetAttribIMsgOnIStg** e recuperados com o [GetAttribIMsgOnIStg](getattribimsgonistg.md). 
  
 **Observação** **GetAttribIMsgOnIStg** e **SetAttribIMsgOnIStg** não operam em todos os objetos **IMessage** . Eles são válidos apenas para objetos **IMessage**-on- **IStorage** retornados por **OpenIMsgOnIStg**. 
  
No parâmetro _lpPropAttrs_ , o número e a posição dos atributos devem corresponder ao número e à posição das marcas de propriedade passadas no parâmetro _lpPropTags_ . 
  
A função **SetAttribIMsgOnIStg** é usada para tornar as propriedades de mensagem somente leitura quando exigidos pelo esquema **IMessage** . O exemplo de provedor de repositório de mensagens o utiliza para essa finalidade. Para obter mais informações, [](mapi-messages.md)consulte messages. 
  

