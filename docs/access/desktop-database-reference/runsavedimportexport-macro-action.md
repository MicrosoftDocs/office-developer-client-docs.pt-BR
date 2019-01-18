---
title: Ação da macro ExecutarImportaçãoOuExportaçãoSalva
TOCTitle: RunSavedImportExport macro action
ms:assetid: b2449c51-ee20-6e50-87f3-a45adc0b0dde
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822018(v=office.15)
ms:contentKeyID: 48547165
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm3022
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: adcc8a2a9462509f4b37d2dbdaf824387ae52a26
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717878"
---
# <a name="runsavedimportexport-macro-action"></a><span data-ttu-id="ec4af-102">Ação da macro ExecutarImportaçãoOuExportaçãoSalva</span><span class="sxs-lookup"><span data-stu-id="ec4af-102">RunSavedImportExport macro action</span></span>

<span data-ttu-id="ec4af-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="ec4af-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ec4af-104">Você pode usar a ação **ExecutarImportaçãoOuExportaçãoSalva** para executar uma especificação de importação ou exportação salva e criada com o Assistente de Importação ou com o Assistente de Exportação.</span><span class="sxs-lookup"><span data-stu-id="ec4af-104">You can use the **RunSavedImportExport** action to run a saved import or export specification that you created by using the Import Wizard or the Export Wizard.</span></span>

> [!NOTE]
> <span data-ttu-id="ec4af-105">[!OBSERVAçãO] This action will not be allowed if the database is not trusted.</span><span class="sxs-lookup"><span data-stu-id="ec4af-105">This action will not be allowed if the database is not trusted.</span></span>

## <a name="setting"></a><span data-ttu-id="ec4af-106">Configuração</span><span class="sxs-lookup"><span data-stu-id="ec4af-106">Setting</span></span>

<span data-ttu-id="ec4af-107">A ação **ExecutarImportaçãoOuExportaçãoSalva** tem o argumento a seguir.</span><span class="sxs-lookup"><span data-stu-id="ec4af-107">The **RunSavedImportExport** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ec4af-108">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="ec4af-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="ec4af-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="ec4af-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ec4af-110"><strong>Nome da exportação de importação salva</strong></span><span class="sxs-lookup"><span data-stu-id="ec4af-110"><strong>Saved Import Export Name</strong></span></span></p></td>
<td><p><span data-ttu-id="ec4af-111">Selecione o nome de uma especificação de importação ou exportação salva, na lista suspensa.</span><span class="sxs-lookup"><span data-stu-id="ec4af-111">Select the name of a saved import or export specification from the drop-down list.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="ec4af-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="ec4af-112">Remarks</span></span>

- <span data-ttu-id="ec4af-113">Esta macro tem o mesmo efeito deste procedimento quando executado no Access:</span><span class="sxs-lookup"><span data-stu-id="ec4af-113">This macro action has the same effect as performing the following procedure in Access:</span></span>
    
  1.  <span data-ttu-id="ec4af-114">Na guia **Dados Externos**, clique em **Importações Salvas** ou em **Exportações Salvas**.</span><span class="sxs-lookup"><span data-stu-id="ec4af-114">On the **External Data** tab, click either **Saved Imports** or **Saved Exports**.</span></span>
    
  2.  <span data-ttu-id="ec4af-115">Na caixa de diálogo **Gerenciar Tarefas de Dados**, na guia **Importações Salvas** ou **Exportações Salvas** (dependendo da sua escolha na etapa anterior), clique na especificação a ser executada.</span><span class="sxs-lookup"><span data-stu-id="ec4af-115">In the **Manage Data Tasks** dialog box, on the **Saved Imports** or **Saved Exports** tab (depending on your choice in the preceding step), click the specification that you want to run.</span></span>
    
  3.  <span data-ttu-id="ec4af-116">Clique em **Executar**.</span><span class="sxs-lookup"><span data-stu-id="ec4af-116">Click **Run**.</span></span>

- <span data-ttu-id="ec4af-117">Antes de executar a ação **ExecutarImportaçãoOuExportaçãoSalva**, verifique se os arquivos de origem e de destino existem, se os dados de origem estão prontos para a importação e se a operação não substituirá acidentalmente nenhum dado do arquivo de destino.</span><span class="sxs-lookup"><span data-stu-id="ec4af-117">Before running the **RunSavedImportExport** action, make sure that the source and destination files exist, the source data is ready for importing, and that the operation will not accidentally overwrite any data in your destination file.</span></span>

- <span data-ttu-id="ec4af-118">Na seção **Consulte Também**, localize links para obter mais informações sobre como salvar e executar especificações de importação e exportação.</span><span class="sxs-lookup"><span data-stu-id="ec4af-118">Find links to more information about saving and running import and export specifications in the **See Also** section.</span></span>

- <span data-ttu-id="ec4af-119">Se o salva de importação ou exportação especificação que você escolher para o argumento **Salvo importar exportar nome** é excluído depois que a macro for criada, o Access exibirá a seguinte mensagem de erro quando a macro será executada: does do **a especificação com o índice especificado não existe. Especifica um índice diferente. ' \* \* \* especificação nome \* \* \* '.**</span><span class="sxs-lookup"><span data-stu-id="ec4af-119">If the saved import or export specification you choose for the **Saved Import Export Name** argument is deleted after the macro is created, Access displays the following error message when the macro is run: **The specification with the specified index does not exist. Specify a different index. '\*\*\*\*\*specification name\*\*\*\*\*'.**</span></span>

