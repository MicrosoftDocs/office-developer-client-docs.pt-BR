---
title: Ação da macro AbrirDiagrama
TOCTitle: OpenDiagram macro action
ms:assetid: 408e7224-02bb-335a-b1b9-cbccbf6e36ec
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192875(v=office.15)
ms:contentKeyID: 48544427
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm154095
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f4273d6858ad98b723d66ba32fe3b9aa7c902d31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288354"
---
# <a name="opendiagram-macro-action"></a><span data-ttu-id="93c3e-102">Ação da macro AbrirDiagrama</span><span class="sxs-lookup"><span data-stu-id="93c3e-102">OpenDiagram macro action</span></span>

<span data-ttu-id="93c3e-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="93c3e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="93c3e-104">Em um projeto do Access, você pode usar a ação **AbrirDiagrama** para abrir um diagrama de banco de dados no modo Design.</span><span class="sxs-lookup"><span data-stu-id="93c3e-104">In an Access project, you can use the **OpenDiagram** action to open a database diagram in Design view.</span></span>

> [!NOTE]
> <span data-ttu-id="93c3e-105">Essa ação não será permitida se o banco de dados não for confiável.</span><span class="sxs-lookup"><span data-stu-id="93c3e-105">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="93c3e-106">Setting</span><span class="sxs-lookup"><span data-stu-id="93c3e-106">Setting</span></span>

<span data-ttu-id="93c3e-107">A ação **AbrirDiagrama** tem os argumentos a seguir.</span><span class="sxs-lookup"><span data-stu-id="93c3e-107">The **OpenDiagram** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="93c3e-108">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="93c3e-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="93c3e-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="93c3e-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93c3e-110"><strong>Nome do Diagrama</strong></span><span class="sxs-lookup"><span data-stu-id="93c3e-110"><strong>Diagram Name</strong></span></span></p></td>
<td><p><span data-ttu-id="93c3e-111">O nome do diagrama de banco de dados que será aberto.</span><span class="sxs-lookup"><span data-stu-id="93c3e-111">The name of the database diagram to open.</span></span> <span data-ttu-id="93c3e-112">A caixa <strong>Nome do Diagrama</strong> da seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros mostra todos os diagramas do banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="93c3e-112">The <strong>Diagram Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all database diagrams in the current database.</span></span> <span data-ttu-id="93c3e-113">Esse é um argumento obrigatório.</span><span class="sxs-lookup"><span data-stu-id="93c3e-113">This is a required argument.</span></span> <span data-ttu-id="93c3e-114">Se você executar uma macro que contém a ação <strong>AbrirDiagrama</strong> em um banco de dados biblioteca, o Microsoft Access procurará o diagrama com esse nome primeiro no banco de dados biblioteca e depois no banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="93c3e-114">If you run a macro containing the <strong>OpenDiagram</strong> action in a library database, Microsoft Access first looks for the diagram with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="93c3e-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="93c3e-115">Remarks</span></span>

<span data-ttu-id="93c3e-116">Esta ação é semelhante a clicar duas vezes em um diagrama de banco de dados do Painel de Navegação ou a clicar com o botão direito do mouse no diagrama de banco de dados do Painel de Navegação e clicar em **Modo Design**.</span><span class="sxs-lookup"><span data-stu-id="93c3e-116">This action is similar to double-clicking a database diagram in the Navigation Pane, or right-clicking the database diagram in the Navigation Pane and then clicking **Design View**.</span></span>

> [!TIP]
> <span data-ttu-id="93c3e-p102">[!DICA] Você pode arrastar um diagrama de banco de dados do Painel de Navegação para uma linha de ação de macro. Isso cria automaticamente uma ação **AbrirDiagrama** que abre o diagrama de banco de dados em modo Design.</span><span class="sxs-lookup"><span data-stu-id="93c3e-p102">You can drag a database diagram from the Navigation Pane to a macro action row. This automatically creates an **OpenDiagram** action that opens the database diagram in Design view.</span></span>

<span data-ttu-id="93c3e-119">Para executar a ação **AbrirDiagrama** em um módulo do VBA (Visual Basic for Applications), use o método **OpenDiagram** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="93c3e-119">To run the **OpenDiagram** action in a Visual Basic for Applications (VBA) module, use the **OpenDiagram** method of the **DoCmd** object.</span></span>

