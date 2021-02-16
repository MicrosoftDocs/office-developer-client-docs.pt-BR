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
# <a name="displaying-dialog-boxes-from-within-a-dll-or-xll"></a><span data-ttu-id="39dd4-104">Exibindo caixas de diálogo de dentro de uma DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="39dd4-104">Displaying Dialog Boxes from Within a DLL or XLL</span></span>

 <span data-ttu-id="39dd4-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="39dd4-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="39dd4-106">Para exibir uma caixa de diálogo Win32 usando, por exemplo, a função Windows SDK **DialogBox**, primeiro você deve obter a instância completa de 32 bits e alças de janela principal para Excel.</span><span class="sxs-lookup"><span data-stu-id="39dd4-106">To display a Win32 dialog box using, for example, the Windows SDK function **DialogBox**, you must first obtain the full 32-bit instance and main window handles for Excel.</span></span> <span data-ttu-id="39dd4-107">For more information, see [Access Excel Instance and Main Window Handles](how-to-access-excel-instance-and-main-window-handles.md).</span><span class="sxs-lookup"><span data-stu-id="39dd4-107">For more information, see [Access Excel Instance and Main Window Handles](how-to-access-excel-instance-and-main-window-handles.md).</span></span> 
  
<span data-ttu-id="39dd4-108">Supondo que seu projeto contenha o recurso de caixa de diálogo, você deve seguir várias etapas para definir a rotina de tratamento de mensagens como a da caixa de diálogo recém-exibida e restaurar a rotina de tratamento de mensagens do Excel quando a caixa de diálogo for fechada.</span><span class="sxs-lookup"><span data-stu-id="39dd4-108">Assuming your project contains the dialog box resource, you must take several steps to set the message-handling routine to that of the newly displayed dialog box and to restore the Excel message handling routine when the dialog box is closed.</span></span> <span data-ttu-id="39dd4-109">O comando [de exemplo fShowDialog](fshowdialog.md) no projeto genérico demonstra o uso das funções do Windows para fazer isso corretamente.</span><span class="sxs-lookup"><span data-stu-id="39dd4-109">The example command [fShowDialog](fshowdialog.md) in the Generic project demonstrates the use of the Windows functions to do this correctly.</span></span> 
  
<span data-ttu-id="39dd4-110">Você também pode exibir caixas de diálogo usando a API de C sem precisar usar funções do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="39dd4-110">You can also display dialog boxes using the C API without having to use Windows SDK functions.</span></span> <span data-ttu-id="39dd4-111">No entanto, os recursos da caixa de diálogo da API de C são muito limitados em comparação com os do Windows, do Visual Basic for Applications (VBA) ou do Microsoft Foundation Classes (MFC).</span><span class="sxs-lookup"><span data-stu-id="39dd4-111">However, the dialog box capabilities of the C API are very limited compared with those of Windows, Visual Basic for Applications (VBA), or the Microsoft Foundation Classes (MFC).</span></span> <span data-ttu-id="39dd4-112">(Por exemplo, caixas de diálogo da API C são sempre modais).</span><span class="sxs-lookup"><span data-stu-id="39dd4-112">(For example, C API dialog boxes are always modal).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="39dd4-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="39dd4-113">See also</span></span>



[<span data-ttu-id="39dd4-114">Criar XLLs</span><span class="sxs-lookup"><span data-stu-id="39dd4-114">Creating XLLs</span></span>](creating-xlls.md)
  
[<span data-ttu-id="39dd4-115">Desenvolver DLLs</span><span class="sxs-lookup"><span data-stu-id="39dd4-115">Developing DLLs</span></span>](developing-dlls.md)
  
[<span data-ttu-id="39dd4-116">Acessar a instância do Excel e as alças da janela principal</span><span class="sxs-lookup"><span data-stu-id="39dd4-116">Access Excel Instance and Main Window Handles</span></span>](how-to-access-excel-instance-and-main-window-handles.md)
  
[<span data-ttu-id="39dd4-117">Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="39dd4-117">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

