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
ms.openlocfilehash: c66ff2338eb5751dbffe392a6a26258fb1c89476
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565834"
---
# <a name="dismissmodeless"></a>DISMISSMODELESS

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define uma função de retorno de chamada que chamadas MAPI quando ele tem descartado uma caixa de diálogo do catálogo de endereços sem janela restrita. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Função definido implementada por:  <br/> |Aplicativos cliente  <br/> |
|Função definido chamada pelo:  <br/> |MAPI  <br/> |
   
```cpp
void (STDMETHODCALLTYPE DISMISSMODELESS)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext
);
```

## <a name="parameters"></a>Parâmetros

 _ulUIParam_
  
> [in] Um valor específico de implementação que geralmente é usado para passar informações de interface de usuário para uma função. Por exemplo, no Microsoft Windows esse parâmetro é o identificador da janela pai para a caixa de diálogo e é do tipo HWND, convertida em um **ULONG_PTR**. Um valor de zero indica que não há nenhuma janela pai. 
    
 _lpvContext_
  
> [in] Ponteiro para um valor arbitrário passado para a função de retorno de chamada quando chamadas de MAPI-lo. Esse valor pode representar um endereço de significância ao aplicativo cliente. Geralmente, para código C++, _lpvContext_ é um ponteiro para o endereço de uma instância do objeto C++. 
    
## <a name="return-value"></a>Valor retornado

None
  
## <a name="remarks"></a>Comentários

Quando o aplicativo cliente invoca uma caixa de diálogo do catálogo de endereços sem janela restrita, ele inclui em seu loop de mensagem do Windows uma chamada para uma função com base em protótipo [ACCELERATEABSDI](accelerateabsdi.md) , que procura e processa as teclas de aceleração. Quando a caixa de diálogo é fechada, chamadas de MAPI o **DISMISSMODELESS** com base em função para que o aplicativo cliente será interrompida chamando o **ACCELERATEABSDI** com base em função. 
  
## <a name="see-also"></a>Confira também



[ADRPARM](adrparm.md)

