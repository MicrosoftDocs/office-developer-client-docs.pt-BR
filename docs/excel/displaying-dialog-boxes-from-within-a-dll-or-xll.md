---
title: Exibindo caixas de diálogo de dentro de uma DLL ou XLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- XLLs [excel 2007], exibindo caixas de diálogo, nas caixas de diálogo [Excel 2007], exibindo por um DLL ou XLL, DLLs [Excel 2007], exibindo caixas de diálogo de
localization_priority: Normal
ms.assetid: e77ac555-331d-41c8-a000-7b178959754d
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: afb21125bc54a2607a997c7b2f7c73ef2f528f28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765274"
---
# <a name="displaying-dialog-boxes-from-within-a-dll-or-xll"></a>Exibindo caixas de diálogo de dentro de uma DLL ou XLL

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Para exibir uma caixa de diálogo Win32 usando, por exemplo, a função do SDK do Windows **DialogBox**, é necessário primeiramente obter a instância de 32 bits completa e as alças da janela principal para o Excel. Para obter mais informações, consulte [acesso Excel instância e identificadores de janela principal](how-to-access-excel-instance-and-main-window-handles.md). 
  
Assumindo que seu projeto contém o recurso de caixa de diálogo, você deve levar várias etapas para definir a rotina de tratamento de mensagens que da caixa de diálogo exibida recentemente e para restaurar a mensagem de Excel rotina de manipulação de quando a caixa de diálogo é fechada. O comando de exemplo [fShowDialog](fshowdialog.md) no projeto genérico demonstra o uso das funções do Windows para fazer isso corretamente. 
  
Você também pode exibir caixas de diálogo usando a API C sem precisar usar funções do SDK do Windows. No entanto, os recursos de caixa de diálogo da API C são muito limitados em comparação com os do Windows, Visual Basic for Applications (VBA) ou o Microsoft Foundation Classes (MFC). (Por exemplo, caixas de diálogo do C API são sempre modais).
  
## <a name="see-also"></a>Confira também



[Criando XLLs](creating-xlls.md)
  
[Developing DLLs](developing-dlls.md)
  
[Acessar a instância do Excel e as alças da janela principal](how-to-access-excel-instance-and-main-window-handles.md)
  
[Funções da API C que podem ser chamadas apenas por um DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

