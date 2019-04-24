---
title: Exibindo caixas de diálogo de dentro de uma DLL ou XLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- XLLs [Excel 2007], exibindo caixas de diálogo de, caixas de diálogo [Excel 2007], exibindo de uma DLL ou XLL, DLLs [Excel 2007], exibindo caixas de diálogo de
localization_priority: Normal
ms.assetid: e77ac555-331d-41c8-a000-7b178959754d
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 7b00430b047fe792afef701d210ccde06dd16216
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310931"
---
# <a name="displaying-dialog-boxes-from-within-a-dll-or-xll"></a>Exibindo caixas de diálogo de dentro de uma DLL ou XLL

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Para exibir uma caixa de diálogo do Win32 usando, por exemplo, a função SDK do Windows **DialogBox**, você deve primeiro obter a instância completa de 32 bits e os identificadores de janela principal para o Excel. Para obter mais informações, consulte [instâncias do Excel e identificadores de janela principal do Access](how-to-access-excel-instance-and-main-window-handles.md). 
  
Supondo que seu projeto contenha o recurso caixa de diálogo, você deve executar várias etapas para definir a rotina de tratamento de mensagens para a da caixa de diálogo exibida recentemente e para restaurar a rotina de tratamento de mensagens do Excel quando a caixa de diálogo é fechada. O exemplo de comando de [fShowDialog](fshowdialog.md) no projeto genérico demonstra o uso das funções do Windows para fazer isso corretamente. 
  
Você também pode exibir caixas de diálogo usando a API C sem ter que usar as funções do Windows SDK. No enTanto, a caixa de diálogo recursos da API C são muito limitadas em comparação com as do Windows, Visual Basic for Applications (VBA) ou Microsoft Foundation classes (MFC). (Por exemplo, as caixas de diálogo da API C são sempre restritas).
  
## <a name="see-also"></a>Confira também



[Como criar XLLs](creating-xlls.md)
  
[Desenvolver DLLs](developing-dlls.md)
  
[Acessar a instância do Excel e as alças da janela principal](how-to-access-excel-instance-and-main-window-handles.md)
  
[Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

