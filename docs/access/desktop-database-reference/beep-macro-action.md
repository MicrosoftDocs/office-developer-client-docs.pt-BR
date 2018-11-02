---
title: Ação de macro AlarmeSonoro (referência de banco de dados da área de trabalho do Access)
TOCTitle: Beep macro action
ms:assetid: 5ca1600f-7934-3b3d-19fd-f305cda0e5d8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194572(v=office.15)
ms:contentKeyID: 48545092
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm11853
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d8ceb39071335b1600f4e371a357126306fbcf2a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922229"
---
# <a name="beep-macro-action"></a><span data-ttu-id="30a0e-102">Ação da macro AlarmeSonoro</span><span class="sxs-lookup"><span data-stu-id="30a0e-102">Beep macro action</span></span>


<span data-ttu-id="30a0e-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="30a0e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="30a0e-104">Você pode usar a ação **AlarmeSonoro** para emitir um tom de alarme sonoro pelo alto-falante do computador.</span><span class="sxs-lookup"><span data-stu-id="30a0e-104">You can use the **Beep** action to sound a beep tone through the computer's speaker.</span></span>

## <a name="setting"></a><span data-ttu-id="30a0e-105">Configuração</span><span class="sxs-lookup"><span data-stu-id="30a0e-105">Setting</span></span>

<span data-ttu-id="30a0e-106">A ação **AlarmeSonoro** não tem nenhum argumento.</span><span class="sxs-lookup"><span data-stu-id="30a0e-106">The **Beep** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="30a0e-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="30a0e-107">Remarks</span></span>

<span data-ttu-id="30a0e-108">Você pode usar a ação **AlarmeSonoro** para sinalizar as seguintes ocorrências:</span><span class="sxs-lookup"><span data-stu-id="30a0e-108">You can use the **Beep** action to signal the following occurrences:</span></span>

  - <span data-ttu-id="30a0e-109">Importantes alterações de tela.</span><span class="sxs-lookup"><span data-stu-id="30a0e-109">Important screen changes have occurred.</span></span>

  - <span data-ttu-id="30a0e-p101">Foram inseridos tipos errados de dados em um controle. Por exemplo, o usuário inseriu dados numéricos em um controle de caixa de texto.</span><span class="sxs-lookup"><span data-stu-id="30a0e-p101">The wrong kind of data has been entered in a control. For example, the user has entered numeric data in a text box control.</span></span>

  - <span data-ttu-id="30a0e-112">Uma macro atingiu um ponto especificado ou concluiu suas ações.</span><span class="sxs-lookup"><span data-stu-id="30a0e-112">A macro has reached a specified point or has completed its actions.</span></span>

<span data-ttu-id="30a0e-113">A frequência e a duração do alarme sonoro dependem do hardware, que pode variar entre computadores.</span><span class="sxs-lookup"><span data-stu-id="30a0e-113">The frequency and duration of the beep depend on the hardware, which may vary between computers.</span></span>

<span data-ttu-id="30a0e-114">Para executar a ação **AlarmeSonoro** em um módulo do VBA (Visual Basic for Applications), use o método **Beep** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="30a0e-114">To run the **Beep** action in a Visual Basic for Applications (VBA) module, use the **Beep** method of the **DoCmd** object.</span></span>

