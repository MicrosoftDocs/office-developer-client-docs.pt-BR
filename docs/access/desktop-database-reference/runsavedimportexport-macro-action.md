---
title: Ação da macro ExecutarImportaçãoOuExportaçãoSalva
TOCTitle: RunSavedImportExport Macro Action
ms:assetid: b2449c51-ee20-6e50-87f3-a45adc0b0dde
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822018(v=office.15)
ms:contentKeyID: 48547165
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm3022
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 48e808fa27e468dd7cb651cb5784627d5064fea0
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870930"
---
# <a name="runsavedimportexport-macro-action"></a><span data-ttu-id="ff839-102">Ação da macro ExecutarImportaçãoOuExportaçãoSalva</span><span class="sxs-lookup"><span data-stu-id="ff839-102">RunSavedImportExport Macro Action</span></span>


<span data-ttu-id="ff839-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="ff839-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ff839-104">Você pode usar a ação **ExecutarImportaçãoOuExportaçãoSalva** para executar uma especificação de importação ou exportação salva e criada com o Assistente de Importação ou com o Assistente de Exportação.</span><span class="sxs-lookup"><span data-stu-id="ff839-104">You can use the **RunSavedImportExport** action to run a saved import or export specification that you created by using the Import Wizard or the Export Wizard.</span></span>


> [!NOTE]
> <P><span data-ttu-id="ff839-p101">[!OBSERVAçãO] This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span><span class="sxs-lookup"><span data-stu-id="ff839-p101">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="ff839-107">Configuração</span><span class="sxs-lookup"><span data-stu-id="ff839-107">Setting</span></span>

<span data-ttu-id="ff839-108">A ação **ExecutarImportaçãoOuExportaçãoSalva** tem o argumento a seguir.</span><span class="sxs-lookup"><span data-stu-id="ff839-108">The **RunSavedImportExport** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ff839-109">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="ff839-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="ff839-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="ff839-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ff839-111"><strong>Nome da exportação de importação salva</strong></span><span class="sxs-lookup"><span data-stu-id="ff839-111"><strong>Saved Import Export Name</strong></span></span></p></td>
<td><p><span data-ttu-id="ff839-112">Selecione o nome de uma especificação de importação ou exportação salva, na lista suspensa.</span><span class="sxs-lookup"><span data-stu-id="ff839-112">Select the name of a saved import or export specification from the drop-down list.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="ff839-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="ff839-113">Remarks</span></span>

  - <span data-ttu-id="ff839-114">Esta macro tem o mesmo efeito deste procedimento quando executado no Access:</span><span class="sxs-lookup"><span data-stu-id="ff839-114">This macro action has the same effect as performing the following procedure in Access:</span></span>
    
    1.  <span data-ttu-id="ff839-115">Na guia **Dados Externos**, clique em **Importações Salvas** ou em **Exportações Salvas**.</span><span class="sxs-lookup"><span data-stu-id="ff839-115">On the **External Data** tab, click either **Saved Imports** or **Saved Exports**.</span></span>
    
    2.  <span data-ttu-id="ff839-116">Na caixa de diálogo **Gerenciar Tarefas de Dados**, na guia **Importações Salvas** ou **Exportações Salvas** (dependendo da sua escolha na etapa anterior), clique na especificação a ser executada.</span><span class="sxs-lookup"><span data-stu-id="ff839-116">In the **Manage Data Tasks** dialog box, on the **Saved Imports** or **Saved Exports** tab (depending on your choice in the preceding step), click the specification that you want to run.</span></span>
    
    3.  <span data-ttu-id="ff839-117">Clique em **Executar**.</span><span class="sxs-lookup"><span data-stu-id="ff839-117">Click **Run**.</span></span>

  - <span data-ttu-id="ff839-118">Antes de executar a ação **ExecutarImportaçãoOuExportaçãoSalva**, verifique se os arquivos de origem e de destino existem, se os dados de origem estão prontos para a importação e se a operação não substituirá acidentalmente nenhum dado do arquivo de destino.</span><span class="sxs-lookup"><span data-stu-id="ff839-118">Before running the **RunSavedImportExport** action, make sure that the source and destination files exist, the source data is ready for importing, and that the operation will not accidentally overwrite any data in your destination file.</span></span>

  - <span data-ttu-id="ff839-119">Na seção **Consulte Também**, localize links para obter mais informações sobre como salvar e executar especificações de importação e exportação.</span><span class="sxs-lookup"><span data-stu-id="ff839-119">Find links to more information about saving and running import and export specifications in the **See Also** section.</span></span>

  - <span data-ttu-id="ff839-120">Se o salva de importação ou exportação especificação que você escolher para o argumento **Salvo importar exportar nome** é excluído depois que a macro for criada, o Access exibirá a seguinte mensagem de erro quando a macro será executada: does do **a especificação com o índice especificado não existe. Especifica um índice diferente. ' \* \* \* especificação nome \* \* \* '.**</span><span class="sxs-lookup"><span data-stu-id="ff839-120">If the saved import or export specification you choose for the **Saved Import Export Name** argument is deleted after the macro is created, Access displays the following error message when the macro is run: **The specification with the specified index does not exist. Specify a different index. '\*\*\*\*\*specification name\*\*\*\*\*'.**</span></span>

