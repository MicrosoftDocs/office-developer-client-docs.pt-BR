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
ms.openlocfilehash: b7d4d758f7031c55aa3a23b662ec8727ea1e0719
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766116"
---
# <a name="accelerateabsdi"></a>ACCELERATEABSDI
 
**Aplica-se a**: Outlook 
  
Define uma função de retorno de chamada para teclas de aceleração do processo em uma caixa de diálogo do catálogo de endereços sem janela restrita. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Função definido implementada por:  <br/> |MAPI  <br/> |
|Função definido chamada pelo:  <br/> |Aplicativos cliente  <br/> |
   
```cpp
BOOL (STDMETHODCALLTYPE ACCELERATEABSDI)( 
  ULONG_PTR ulUIParam,
  LPVOID lpvmsg
);
```

## <a name="parameters"></a>Parâmetros

 _ulUIParam_
  
> [in] Um valor específico de implementação usado para passar as informações de interface de usuário para uma função. Em aplicativos em execução no Microsoft Windows, _ulUIParam_ é o identificador da janela pai para uma caixa de diálogo e do tipo HWND, convertida em um **ULONG_PTR**. Um valor de zero indica que não há nenhuma janela pai. 
    
 _lpvmsg_
  
> [in] Ponteiro para uma mensagem do Windows.
    
## <a name="return-value"></a>Valor retornado

Uma função com o protótipo **ACCELERATEABSDI** retorna TRUE se ele lida com a mensagem. 
  
## <a name="remarks"></a>Comentários

Uma função com base em protótipo **ACCELERATEABSDI** é usada somente com uma caixa de diálogo sem janela restrita, ou seja, apenas se o aplicativo cliente tiver definido o sinalizador DIALOG_SDI no membro _ulFlags_ da estrutura [ADRPARM](adrparm.md) . 
  
Uma caixa de diálogo sem janela restrita compartilha um loop de mensagem do aplicativo cliente Windows, em vez de seu próprio loop. O aplicativo, que controla o loop de mensagens, não sabe quais teclas de aceleração os usos de diálogo, portanto, ele chama um **ACCELERATEABSDI** com base função para testar e agir em teclas de aceleração como CTRL + P para impressão. 
  
Chamadas de loop de mensagem do cliente a **ACCELERATEABSDI** com base em função quando o cliente invoca uma caixa de diálogo do catálogo de endereços sem janela restrita com o método [IAddrBook::Address](iaddrbook-address.md) . Essa chamada é encerrada quando uma função com base no protótipo de função [DISMISSMODELESS](dismissmodeless.md) chamadas de MAPI. 
  

