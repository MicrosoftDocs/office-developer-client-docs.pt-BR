---
title: Implementar objetos em C
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 24fc4d78-726d-40ff-bad2-25dc298bd51a
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: d07d756abded137d3268daf7dd0998f0c953cb1d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563944"
---
# <a name="implementing-objects-in-c"></a>Implementar objetos em C

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Aplicativos cliente e provedores de serviços escritas em C definem os objetos MAPI criando uma estrutura de dados e uma matriz de ponteiros de função ordenada conhecido como uma tabela de função virtual, ou vtable. Um ponteiro para o vtable deve ser o primeiro membro da estrutura de dados.
  
O vtable em si, não há um ponteiro para cada método em cada interface suportado pelo objeto. A ordem dos ponteiros deve seguir a ordem dos métodos na interface especificação publicado no arquivo de cabeçalho Mapidefs.h. Cada ponteiro de função no vtable é definido como o endereço da implementação do método. No C++, o compilador automaticamente configura o vtable. Na opção C, ele não faz. 
  
A ilustração a seguir mostra como isso funciona. A caixa na extrema esquerda representa um cliente que precisa usar um objeto de provedor de serviço. Através da sessão, o cliente obtém um ponteiro para o objeto, **lpObject**. O vtable aparece primeiro no objeto seguido por métodos e dados particulares. O ponteiro vtable aponta para o vtable real, que contém ponteiros para cada uma das implementações dos métodos na interface do. 
  
**Object implementation**
  
![Implementação de objeto] (media/amapi_42.gif "Implementação de objeto")
  
O exemplo de código a seguir mostra como um provedor de serviços de C pode definir um objeto simples de status. O primeiro membro for o ponteiro vtable; o restante do objeto é composto de membros de dados. 
  
```C
typedef struct _MYSTATUSOBJECT
{
    const STATUS_Vtbl FAR *lpVtbl;
    ULONG              cRef;
    ANOTHEROBJ        *pObj;
    LPMAPIPROP         lpProp;
    LPFREEBUFFER       lpFreeBuf;
} MYSTATUSOBJECT, *LPMYSTATUSOBJ;
 
```

Como este objeto é um objeto de status, o vtable inclui ponteiros para implementações de cada um dos métodos no [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) interface, bem como ponteiros para implementações de cada um dos métodos nas interfaces base — **IUnknown **e **IMAPIProp**. A ordem dos métodos no vtable corresponde a ordem especificada como definido no arquivo de cabeçalho Mapidefs.h.
  
```js
static const MYOBJECT_Vtbl vtblSTATUS =
{
    STATUS_QueryInterface,
    STATUS_AddRef,
    STATUS_Release,
    STATUS_GetLastError,
    STATUS_SaveChanges,
    STATUS_GetProps,
    STATUS_GetPropList,
    STATUS_OpenProperty,
    STATUS_SetProps,
    STATUS_DeleteProps,
    STATUS_CopyTo,
    STATUS_CopyProps,
    STATUS_GetNamesFromIDs,
    STATUS_GetIDsFromNames,
    STATUS_ValidateState,
    STATUS_SettingsDialog,
    STATUS_ChangePassword,
    STATUS_FlushQueues
};
 
```

Clientes e provedores de serviços escritas em C usam objetos indiretamente por meio do vtable e adicione um ponteiro de objeto como o primeiro parâmetro em cada chamada. Cada chamada para um método de interface MAPI requer um ponteiro para o objeto sendo chamado como seu primeiro parâmetro. C++ define um ponteiro especial conhecido como o ponteiro **this** para essa finalidade. O compilador C++ adiciona implicitamente o ponteiro **this** como o primeiro parâmetro para cada chamada de método. No C não há nenhuma dessas ponteiro; ela deve ser explicitamente adicionada. 
  
O código a seguir demonstra como um cliente pode fazer uma chamada para uma instância do MYSTATUSOBJECT:
  
```C
lpMyObj->lpVtbl->ValidateState(lpMyObj, ulUIParam, ulFlags);
 
```

## <a name="see-also"></a>Confira também

- [Implementar objetos de MAPI](implementing-mapi-objects.md)

