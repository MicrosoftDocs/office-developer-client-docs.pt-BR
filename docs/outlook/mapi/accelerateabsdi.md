---
title: ACCELERATEABSDI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ACCELERATEABSDI
api_type:
- HeaderDef
ms.assetid: da67dcf4-1411-4fc9-992c-115485019bd3
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 46e87caa68a45a188272340db408c52546f02a57
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420371"
---
# <a name="accelerateabsdi"></a>ACCELERATEABSDI
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define uma função de retorno de chamada para processar teclas de aceleração em uma caixa de diálogo do catálogo de endereços sem restrições. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
|Função definida implementada por:  <br/> |MAPI  <br/> |
|Função definida chamada por:  <br/> |Aplicativos cliente  <br/> |
   
```cpp
BOOL (STDMETHODCALLTYPE ACCELERATEABSDI)( 
  ULONG_PTR ulUIParam,
  LPVOID lpvmsg
);
```

## <a name="parameters"></a>Parâmetros

 _ulUIParam_
  
> no Um valor específico de implementação usado para passar informações da interface do usuário para uma função. Em aplicativos executados no Microsoft Windows, _ulUIParam_ é o identificador da janela pai de uma caixa de diálogo e é do tipo HWND, CAST para um **ULONG_PTR**. Um valor igual A zero indica que não há janela pai. 
    
 _lpvmsg_
  
> no Ponteiro para uma mensagem do Windows.
    
## <a name="return-value"></a>Valor de retorno

Uma função com o protótipo **ACCELERATEABSDI** retorna true se ele lida com a mensagem. 
  
## <a name="remarks"></a>Comentários

Uma função com base no protótipo **ACCELERATEABSDI** é usada apenas com uma caixa de diálogo sem janela restrita, ou seja, somente se o aplicativo cliente tiver definido o sinalizador DIALOG_SDI no membro _Parâmetroulflags_ da estrutura [ADRPARM](adrparm.md) . 
  
Uma caixa de diálogo sem janela restrita compartilha o loop de mensagem do Windows do aplicativo cliente, em vez de ter seu próprio loop. O aplicativo, que controla o loop de mensagem, não sabe quais teclas de aceleração a caixa de diálogo usa, portanto, ele chama uma função baseada em **ACCELERATEABSDI** para testar e agir em teclas de aceleração, como CTRL + P para impressão. 
  
O loop de mensagens de um cliente chama a função baseada em **ACCELERATEABSDI** quando o cliente invoca uma caixa de diálogo do catálogo de endereços sem restrições com o método de [endereço IAddrBook::](iaddrbook-address.md) . Essa chamada é terminada quando MAPI chama uma função com base no protótipo de função [DISMISSMODELESS](dismissmodeless.md) . 
  

