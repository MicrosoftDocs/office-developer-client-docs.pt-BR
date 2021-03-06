---
title: DISMISSMODELESS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DISMISSMODELESS
api_type:
- COM
ms.assetid: ef93ef3d-c159-40ae-9b8d-0af8a0567565
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: dd962515a85cb6a4b8661a0fd5294cea55cd6e96
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428183"
---
# <a name="dismissmodeless"></a>DISMISSMODELESS

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define uma função de retorno de chamada que MAPI chama quando descarta uma caixa de diálogo de agenda sem modo. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Função definida implementada por:  <br/> |Aplicativos do cliente  <br/> |
|Função definida chamada por:  <br/> |MAPI  <br/> |
   
```cpp
void (STDMETHODCALLTYPE DISMISSMODELESS)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext
);
```

## <a name="parameters"></a>Parâmetros

 _ulUIParam_
  
> [in] Um valor específico de implementação normalmente usado para passar informações da interface do usuário para uma função. Por exemplo, no Microsoft Windows esse parâmetro é o identificador da janela pai da caixa de diálogo e é do tipo HWND, cast em um **ULONG_PTR**. Um valor zero indica que não há janela pai. 
    
 _lpvContext_
  
> [in] Ponteiro para um valor arbitrário passado para a função de retorno de chamada quando MAPI o chama. Esse valor pode representar um endereço significativo para o aplicativo cliente. Normalmente, para código C++,  _lpvContext_ é um ponteiro para o endereço de uma instância de objeto C++. 
    
## <a name="return-value"></a>Valor de retorno

Nenhum
  
## <a name="remarks"></a>Comentários

Quando o aplicativo cliente invoca uma caixa de diálogo de livro de endereços sem janelas, ele inclui em seu loop de mensagem do Windows uma chamada para uma função com base no protótipo [ACCELERATEABSDI,](accelerateabsdi.md) que verifica e processa teclas aceleradoras. Quando a caixa de diálogo é fechada, MAPI chama a função baseada **DISMISSMODELESS** para que o aplicativo cliente pare de chamar a **função baseada ACCELERATEABSDI.** 
  
## <a name="see-also"></a>Confira também



[ADRPARM](adrparm.md)

