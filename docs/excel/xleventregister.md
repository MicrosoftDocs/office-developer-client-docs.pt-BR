---
title: xlEventRegister
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b98637d4-02e3-4dbd-8be5-6b46d32980c6
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: d837d87c479f70f0184a7cf1612dea5ab8c99e6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765467"
---
# <a name="xleventregister"></a>xlEventRegister

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Usado para registrar um manipulador de eventos. Introduzido no Excel 2010.
  
```vb
Excel12(xlEventRegister, LPXLOPER12 pxRes, 2, LPXLOPER12 pxProcedure, LPXLOPER12 pxEvent);
```

## <a name="parameters"></a>Par�metros

 _pxProcedure_ (**xltypeStr**)
  
O nome da função handler evento como ele aparece no código DLL.
  
 _pxEvent_ (**xltypeInt**)
  
O evento manipulado pela função designada no parâmetro _pxProcedure_ . 
  
Iniciando no Excel 2010, Excel suporta os seguintes eventos:
  
|**Event**|**Descrição**|
|:-----|:-----|
|**xleventCalculationEnded** <br/> |Acionado quando um cálculo do Excel completa. Você pode liberar quaisquer recursos alocados durante o cálculo após este evento.  <br/> |
|**xleventCalculationCanceled** <br/> |Acionado quando o usuário interrompe o cálculo. XLL deve parar qualquer atividades assíncronas. O evento CalculationEnded é disparado imediatamente após este evento.  <br/> |
   
## <a name="property-valuereturn-value"></a>Propriedade valor/valor de retorno

Se tiver êxito, retornará **TRUE** (**xltypeBool**). Se for bem sucedida, retornará **FALSE**.
  
## <a name="see-also"></a>Confira também



[Funções assíncronas definidas pelo usuário](asynchronous-user-defined-functions.md)

