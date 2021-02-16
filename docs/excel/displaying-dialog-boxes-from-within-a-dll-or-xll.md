---
title: Exibindo caixas de diálogo de dentro de uma DLL ou XLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- xlls [excel 2007], exibindo caixas de diálogo de,caixas de diálogo [Excel 2007], exibindo de uma DLL ou XLL,DLLs [Excel 2007], exibindo caixas de diálogo de
localization_priority: Normal
ms.assetid: e77ac555-331d-41c8-a000-7b178959754d
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 7b00430b047fe792afef701d210ccde06dd16216
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417865"
---
# <a name="displaying-dialog-boxes-from-within-a-dll-or-xll"></a>Exibindo caixas de diálogo de dentro de uma DLL ou XLL

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Para exibir uma caixa de diálogo Win32 usando, por exemplo, a função Windows SDK **DialogBox**, primeiro você deve obter a instância completa de 32 bits e alças de janela principal para Excel. For more information, see [Access Excel Instance and Main Window Handles](how-to-access-excel-instance-and-main-window-handles.md). 
  
Supondo que seu projeto contenha o recurso de caixa de diálogo, você deve seguir várias etapas para definir a rotina de tratamento de mensagens como a da caixa de diálogo recém-exibida e restaurar a rotina de tratamento de mensagens do Excel quando a caixa de diálogo for fechada. O comando [de exemplo fShowDialog](fshowdialog.md) no projeto genérico demonstra o uso das funções do Windows para fazer isso corretamente. 
  
Você também pode exibir caixas de diálogo usando a API de C sem precisar usar funções do SDK do Windows. No entanto, os recursos da caixa de diálogo da API de C são muito limitados em comparação com os do Windows, do Visual Basic for Applications (VBA) ou do Microsoft Foundation Classes (MFC). (Por exemplo, caixas de diálogo da API C são sempre modais).
  
## <a name="see-also"></a>Confira também



[Criar XLLs](creating-xlls.md)
  
[Desenvolver DLLs](developing-dlls.md)
  
[Acessar a instância do Excel e as alças da janela principal](how-to-access-excel-instance-and-main-window-handles.md)
  
[Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

