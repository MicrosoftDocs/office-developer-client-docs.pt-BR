---
title: Exibir as caixas de diálogo de dentro de uma DLL ou XLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- XLLs [excel 2007], exibindo caixas de diálogo, nas caixas de diálogo [Excel 2007], exibindo por um DLL ou XLL, DLLs [Excel 2007], exibindo caixas de diálogo de
localization_priority: Normal
ms.assetid: e77ac555-331d-41c8-a000-7b178959754d
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: afb21125bc54a2607a997c7b2f7c73ef2f528f28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765274"
---
# <a name="displaying-dialog-boxes-from-within-a-dll-or-xll"></a><span data-ttu-id="26791-104">Exibir as caixas de diálogo de dentro de uma DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="26791-104">Displaying Dialog Boxes from Within a DLL or XLL</span></span>

 <span data-ttu-id="26791-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="26791-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="26791-106">Para exibir uma caixa de diálogo Win32 usando, por exemplo, a função do SDK do Windows **DialogBox**, é necessário primeiramente obter a instância de 32 bits completa e as alças da janela principal para o Excel.</span><span class="sxs-lookup"><span data-stu-id="26791-106">To display a Win32 dialog box using, for example, the Windows SDK function **DialogBox**, you must first obtain the full 32-bit instance and main window handles for Excel.</span></span> <span data-ttu-id="26791-107">Para obter mais informações, consulte [acesso Excel instância e identificadores de janela principal](how-to-access-excel-instance-and-main-window-handles.md).</span><span class="sxs-lookup"><span data-stu-id="26791-107">For more information, see [Access Excel Instance and Main Window Handles](how-to-access-excel-instance-and-main-window-handles.md).</span></span> 
  
<span data-ttu-id="26791-108">Assumindo que seu projeto contém o recurso de caixa de diálogo, você deve levar várias etapas para definir a rotina de tratamento de mensagens que da caixa de diálogo exibida recentemente e para restaurar a mensagem de Excel rotina de manipulação de quando a caixa de diálogo é fechada.</span><span class="sxs-lookup"><span data-stu-id="26791-108">Assuming your project contains the dialog box resource, you must take several steps to set the message-handling routine to that of the newly displayed dialog box and to restore the Excel message handling routine when the dialog box is closed.</span></span> <span data-ttu-id="26791-109">O comando de exemplo [fShowDialog](fshowdialog.md) no projeto genérico demonstra o uso das funções do Windows para fazer isso corretamente.</span><span class="sxs-lookup"><span data-stu-id="26791-109">The example command [fShowDialog](fshowdialog.md) in the Generic project demonstrates the use of the Windows functions to do this correctly.</span></span> 
  
<span data-ttu-id="26791-110">Você também pode exibir caixas de diálogo usando a API C sem precisar usar funções do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="26791-110">You can also display dialog boxes using the C API without having to use Windows SDK functions.</span></span> <span data-ttu-id="26791-111">No entanto, os recursos de caixa de diálogo da API C são muito limitados em comparação com os do Windows, Visual Basic for Applications (VBA) ou o Microsoft Foundation Classes (MFC).</span><span class="sxs-lookup"><span data-stu-id="26791-111">However, the dialog box capabilities of the C API are very limited compared with those of Windows, Visual Basic for Applications (VBA), or the Microsoft Foundation Classes (MFC).</span></span> <span data-ttu-id="26791-112">(Por exemplo, caixas de diálogo do C API são sempre modais).</span><span class="sxs-lookup"><span data-stu-id="26791-112">(For example, C API dialog boxes are always modal).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="26791-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="26791-113">See also</span></span>



[<span data-ttu-id="26791-114">Criar XLLs</span><span class="sxs-lookup"><span data-stu-id="26791-114">Creating XLLs</span></span>](creating-xlls.md)
  
[<span data-ttu-id="26791-115">Developing DLLs</span><span class="sxs-lookup"><span data-stu-id="26791-115">Developing DLLs</span></span>](developing-dlls.md)
  
[<span data-ttu-id="26791-116">Acessar a instância do Excel e as alças da janela principal</span><span class="sxs-lookup"><span data-stu-id="26791-116">Access Excel Instance and Main Window Handles</span></span>](how-to-access-excel-instance-and-main-window-handles.md)
  
[<span data-ttu-id="26791-117">Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="26791-117">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

