---
title: xlEventRegister
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b98637d4-02e3-4dbd-8be5-6b46d32980c6
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 00c222efce6925c3f691eb2b799adf687c22082c
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160276"
---
# <a name="xleventregister"></a>xlEventRegister

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Usado para registrar um manipulador de eventos. Introduzido no Excel 2010.
  
```vb
Excel12(xlEventRegister, LPXLOPER12 pxRes, 2, LPXLOPER12 pxProcedure, LPXLOPER12 pxEvent);
```

## <a name="parameters"></a>Parâmetros

 _pxProcedure_ (**xltypeStr**)
  
O nome da função do manipulador de eventos conforme ele aparece no código de DLL.
  
 _pxEvent_ (**xltypeInt**)
  
O evento manipulado pela função designada no parâmetro _pxProcedure_ . 
  
A partir do Excel 2010, o Excel oferece suporte aos seguintes eventos:
  
|**Evento**|**Descrição**|
|:-----|:-----|
|**xleventCalculationEnded** <br/> |Gerado quando o Excel conclui um cálculo. Você pode liberar todos os recursos alocados durante o cálculo após este evento.  <br/> |
|**xleventCalculationCanceled** <br/> |Gerado quando o usuário interrompe o cálculo. O XLL deve interromper qualquer atividade assíncrona. O evento CalculationEnded é gerado imediatamente após este evento.  <br/> |
   
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

Se tiver êxito, pxRes (**xltypeInt**) tem um valor > 0. Se não tiver êxito, pxRes = = 0.
  
## <a name="see-also"></a>Confira também



[Funções assíncronas definidas pelo usuário](asynchronous-user-defined-functions.md)

