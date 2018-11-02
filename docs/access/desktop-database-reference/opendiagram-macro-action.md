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
ms.openlocfilehash: c170c9d02967cb04b387d9f549ad77933d1f55b8
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925643"
---
# <a name="opendiagram-macro-action"></a><span data-ttu-id="a440f-102">Ação da macro AbrirDiagrama</span><span class="sxs-lookup"><span data-stu-id="a440f-102">OpenDiagram macro action</span></span>


<span data-ttu-id="a440f-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="a440f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a440f-104">Em um projeto do Access, você pode usar a ação **AbrirDiagrama** para abrir um diagrama de banco de dados no modo Design.</span><span class="sxs-lookup"><span data-stu-id="a440f-104">In an Access project, you can use the **OpenDiagram** action to open a database diagram in Design view.</span></span>


> [!NOTE]
> <P><span data-ttu-id="a440f-p101">[!OBSERVAçãO] This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span><span class="sxs-lookup"><span data-stu-id="a440f-p101">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="a440f-107">Configuração</span><span class="sxs-lookup"><span data-stu-id="a440f-107">Setting</span></span>

<span data-ttu-id="a440f-108">A ação **AbrirDiagrama** tem os argumentos a seguir.</span><span class="sxs-lookup"><span data-stu-id="a440f-108">The **OpenDiagram** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a440f-109">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="a440f-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="a440f-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="a440f-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a440f-111"><strong>Nome do Diagrama</strong></span><span class="sxs-lookup"><span data-stu-id="a440f-111"><strong>Diagram Name</strong></span></span></p></td>
<td><p><span data-ttu-id="a440f-112">O nome do diagrama de banco de dados para abrir.</span><span class="sxs-lookup"><span data-stu-id="a440f-112">The name of the database diagram to open.</span></span> <span data-ttu-id="a440f-113">A caixa <strong>Nome do diagrama</strong> na seção <strong>Argumentos da ação</strong> do painel de tarefas do construtor de macros mostra todos os diagramas de banco de dados no banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="a440f-113">The <strong>Diagram Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all database diagrams in the current database.</span></span> <span data-ttu-id="a440f-114">Este é um argumento obrigatório.</span><span class="sxs-lookup"><span data-stu-id="a440f-114">This is a required argument.</span></span> <span data-ttu-id="a440f-115">Se você executar uma macro que contém a ação <strong>AbrirDiagrama</strong> em um banco de dados biblioteca, o Microsoft Access procurará o diagrama com esse nome primeiro no banco de dados biblioteca e depois no banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="a440f-115">If you run a macro containing the <strong>OpenDiagram</strong> action in a library database, Microsoft Access first looks for the diagram with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a440f-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="a440f-116">Remarks</span></span>

<span data-ttu-id="a440f-117">Esta ação é semelhante a clicar duas vezes em um diagrama de banco de dados do Painel de Navegação ou a clicar com o botão direito do mouse no diagrama de banco de dados do Painel de Navegação e clicar em **Modo Design**.</span><span class="sxs-lookup"><span data-stu-id="a440f-117">This action is similar to double-clicking a database diagram in the Navigation Pane, or right-clicking the database diagram in the Navigation Pane and then clicking **Design View**.</span></span>


> [!TIP]
> <P><span data-ttu-id="a440f-p103">[!DICA] Você pode arrastar um diagrama de banco de dados do Painel de Navegação para uma linha de ação de macro. Isso cria automaticamente uma ação <STRONG>AbrirDiagrama</STRONG> que abre o diagrama de banco de dados em modo Design.</span><span class="sxs-lookup"><span data-stu-id="a440f-p103">You can drag a database diagram from the Navigation Pane to a macro action row. This automatically creates an <STRONG>OpenDiagram</STRONG> action that opens the database diagram in Design view.</span></span></P>



<span data-ttu-id="a440f-120">Para executar a ação **AbrirDiagrama** em um módulo do VBA (Visual Basic for Applications), use o método **OpenDiagram** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="a440f-120">To run the **OpenDiagram** action in a Visual Basic for Applications (VBA) module, use the **OpenDiagram** method of the **DoCmd** object.</span></span>

