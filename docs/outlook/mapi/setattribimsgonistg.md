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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428827"
---
# <a name="setattribimsgonistg"></a>SetAttribIMsgOnIStg

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define ou altera atributos de propriedades em um objeto [IMessage](imessageimapiprop.md) fornecido pela [função OpenIMsgOnIStg.](openimsgonistg.md) 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Imessage.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de armazenamento de mensagens  <br/> |
   
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
  
> [in] Ponteiro para o objeto para o qual os atributos de propriedade estão sendo definidos. 
    
 _lpPropTags_
  
> [in] Ponteiro para uma [estrutura SPropTagArray](sproptagarray.md) contendo uma matriz de marcas de propriedade indicando as propriedades para as quais os atributos de propriedade estão sendo definidos. 
    
 _lpPropAttrs_
  
> [in] Ponteiro para uma [estrutura SPropAttrArray](spropattrarray.md) listando os atributos de propriedade a definir. 
    
 _lppPropProblems_
  
> [out] Ponteiro para a estrutura [SPropProblemArray](spropproblemarray.md) retornada contendo um conjunto de problemas de propriedade. Essa estrutura identifica problemas encontrados se **SetAttribIMsgOnIStg** foi capaz de definir algumas propriedades, mas não todas. Se um ponteiro para NULL for passado no parâmetro  _lppPropProblems,_ nenhuma matriz de problema de propriedade será retornada, mesmo se algumas propriedades não foram definidas. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
MAPI_W_ERRORS_RETURNED 
  
> A chamada foi bem-sucedida em geral, mas uma ou mais propriedades não puderam ser acessadas e foram retornadas com um tipo de propriedade de PT_ERROR.
    
## <a name="remarks"></a>Comentários

Atributos de propriedade só podem ser acessados em objetos de propriedade, ou seja, objetos que implementam o [IMAPIProp : interface IUnknown.](imapipropiunknown.md) Para disponibilizar propriedades MAPI em um objeto de armazenamento estruturado OLE, [OpenIMsgOnIStg](openimsgonistg.md) cria um [IMessage : objeto IMAPIProp](imessageimapiprop.md) sobre o objeto **IStorage** OLE. Os atributos de propriedade nesses objetos podem ser definidos ou alterados com **SetAttribIMsgOnIStg** e recuperados com [GetAttribIMsgOnIStg](getattribimsgonistg.md). 
  
 **Observação** **GetAttribIMsgOnIStg** e **SetAttribIMsgOnIStg** não operam em todos os **objetos IMessage.** Eles só são **válidos para objetos IMessage**-on-IStorage retornados por **OpenIMsgOnIStg**.  
  
No parâmetro _lpPropAttrs,_ o número e a posição dos atributos devem corresponder ao número e à posição das marcas de propriedade passadas no parâmetro _lpPropTags._ 
  
A **função SetAttribIMsgOnIStg** é usada para tornar as propriedades da mensagem somente leitura quando exigido pelo esquema **IMessage.** O provedor de armazenamento de mensagens de exemplo o usa para essa finalidade. Para obter mais informações, consulte [Mensagens.](mapi-messages.md) 
  

