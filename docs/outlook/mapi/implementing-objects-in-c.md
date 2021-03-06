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
ms.openlocfilehash: 6026e697cc31545bf7ef518fcbd33ea8db48af5d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414939"
---
# <a name="implementing-objects-in-c"></a>Implementar objetos em C

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os aplicativos cliente e provedores de serviços escritos em C definem objetos MAPI criando uma estrutura de dados e uma matriz de ponteiros de função ordenada conhecidos como uma tabela de funções virtuais ou vtable. Um ponteiro para a vtable deve ser o primeiro membro da estrutura de dados.
  
Na própria vtable, há um ponteiro para cada método em cada interface com suporte do objeto. A ordem dos ponteiros deve seguir a ordem dos métodos na especificação da interface publicada no arquivo de header Mapidefs.h. Cada ponteiro de função na vtable é definido como o endereço da implementação real do método. Em C++, o compilador configura automaticamente a vtable. Em C, não. 
  
A ilustração a seguir mostra como isso funciona. A caixa à esquerda representa um cliente que precisa usar um objeto de provedor de serviços. Durante a sessão, o cliente obtém um ponteiro para o objeto, **lpObject**. A vtable aparece primeiro no objeto, seguida de dados e métodos privados. O ponteiro vtable aponta para a vtable real, que contém ponteiros para cada uma das implementações dos métodos na interface. 
  
**Object implementation**
  
![Implementação de objeto de](media/amapi_42.gif "implementação de objeto")
  
O exemplo de código a seguir mostra como um provedor de serviços C pode definir um objeto de status simples. O primeiro membro é o ponteiro vtable; o restante do objeto é feito de membros de dados. 
  
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

Como esse objeto é um objeto de status, a vtable inclui ponteiros para implementações de cada um dos métodos na interface [IMAPIStatus : IMAPIProp,](imapistatusimapiprop.md) bem como ponteiros para implementações de cada um dos métodos nas interfaces base — **IUnknown** e **IMAPIProp**. A ordem dos métodos na vtable corresponde à ordem especificada, conforme definido no arquivo de header Mapidefs.h.
  
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

Clientes e provedores de serviços escritos em C usam objetos indiretamente através da vtable e adicionam um ponteiro de objeto como o primeiro parâmetro em cada chamada. Todas as chamadas para um método de interface MAPI exigem um ponteiro para o objeto que está sendo chamado como seu primeiro parâmetro. O C++ define um ponteiro especial conhecido **como ponteiro** para essa finalidade. O compilador C++ adiciona implicitamente esse **ponteiro** como o primeiro parâmetro a cada chamada de método. Em C, não existe esse ponteiro; ela deve ser adicionada explicitamente. 
  
O código a seguir demonstra como um cliente pode fazer uma chamada para uma instância de MYSTATUSOBJECT:
  
```C
lpMyObj->lpVtbl->ValidateState(lpMyObj, ulUIParam, ulFlags);
 
```

## <a name="see-also"></a>Confira também

- [Implementando objetos MAPI](implementing-mapi-objects.md)

