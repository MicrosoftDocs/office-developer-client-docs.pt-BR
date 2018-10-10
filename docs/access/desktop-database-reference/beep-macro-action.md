---
title: Ação de Macro AlarmeSonoro (referência de banco de dados da área de trabalho do Access)
TOCTitle: Beep Macro Action
ms:assetid: 5ca1600f-7934-3b3d-19fd-f305cda0e5d8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194572(v=office.15)
ms:contentKeyID: 48545092
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm11853
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7024734b09544042fa58b8cd95127d8195e5788a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464761"
---
# <a name="beep-macro-action"></a><span data-ttu-id="cfbc1-102">Ação de macro AlarmeSonoro</span><span class="sxs-lookup"><span data-stu-id="cfbc1-102">Beep Macro Action</span></span>


<span data-ttu-id="cfbc1-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="cfbc1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="cfbc1-104">Você pode usar a ação **AlarmeSonoro** para emitir um tom de alarme sonoro pelo alto-falante do computador.</span><span class="sxs-lookup"><span data-stu-id="cfbc1-104">You can use the **Beep** action to sound a beep tone through the computer's speaker.</span></span>

## <a name="setting"></a><span data-ttu-id="cfbc1-105">Configuração</span><span class="sxs-lookup"><span data-stu-id="cfbc1-105">Setting</span></span>

<span data-ttu-id="cfbc1-106">A ação **AlarmeSonoro** não tem nenhum argumento.</span><span class="sxs-lookup"><span data-stu-id="cfbc1-106">The **Beep** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfbc1-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="cfbc1-107">Remarks</span></span>

<span data-ttu-id="cfbc1-108">Você pode usar a ação **AlarmeSonoro** para sinalizar as seguintes ocorrências:</span><span class="sxs-lookup"><span data-stu-id="cfbc1-108">You can use the **Beep** action to signal the following occurrences:</span></span>

  - <span data-ttu-id="cfbc1-109">Importantes alterações de tela.</span><span class="sxs-lookup"><span data-stu-id="cfbc1-109">Important screen changes have occurred.</span></span>

  - <span data-ttu-id="cfbc1-p101">Foram inseridos tipos errados de dados em um controle. Por exemplo, o usuário inseriu dados numéricos em um controle de caixa de texto.</span><span class="sxs-lookup"><span data-stu-id="cfbc1-p101">The wrong kind of data has been entered in a control. For example, the user has entered numeric data in a text box control.</span></span>

  - <span data-ttu-id="cfbc1-112">Uma macro atingiu um ponto especificado ou concluiu suas ações.</span><span class="sxs-lookup"><span data-stu-id="cfbc1-112">A macro has reached a specified point or has completed its actions.</span></span>

<span data-ttu-id="cfbc1-113">A frequência e a duração do alarme sonoro dependem do hardware, que pode variar entre computadores.</span><span class="sxs-lookup"><span data-stu-id="cfbc1-113">The frequency and duration of the beep depend on the hardware, which may vary between computers.</span></span>

<span data-ttu-id="cfbc1-114">Para executar a ação **AlarmeSonoro** em um módulo do VBA (Visual Basic for Applications), use o método **Beep** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="cfbc1-114">To run the **Beep** action in a Visual Basic for Applications (VBA) module, use the **Beep** method of the **DoCmd** object.</span></span>

