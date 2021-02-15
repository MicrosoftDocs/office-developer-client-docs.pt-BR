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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309169"
---
# <a name="runsavedimportexport-macro-action"></a><span data-ttu-id="c5f54-102">Ação da macro ExecutarImportaçãoOuExportaçãoSalva</span><span class="sxs-lookup"><span data-stu-id="c5f54-102">RunSavedImportExport macro action</span></span>

<span data-ttu-id="c5f54-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c5f54-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c5f54-104">Você pode usar a ação **ExecutarImportaçãoOuExportaçãoSalva** para executar uma especificação de importação ou exportação salva e criada com o Assistente de Importação ou com o Assistente de Exportação.</span><span class="sxs-lookup"><span data-stu-id="c5f54-104">You can use the **RunSavedImportExport** action to run a saved import or export specification that you created by using the Import Wizard or the Export Wizard.</span></span>

> [!NOTE]
> <span data-ttu-id="c5f54-105">Essa ação não será permitida se o banco de dados não for confiável.</span><span class="sxs-lookup"><span data-stu-id="c5f54-105">This action will not be allowed if the database is not trusted.</span></span>

## <a name="setting"></a><span data-ttu-id="c5f54-106">Setting</span><span class="sxs-lookup"><span data-stu-id="c5f54-106">Setting</span></span>

<span data-ttu-id="c5f54-107">A ação **ExecutarImportaçãoOuExportaçãoSalva** tem o argumento a seguir.</span><span class="sxs-lookup"><span data-stu-id="c5f54-107">The **RunSavedImportExport** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c5f54-108">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="c5f54-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="c5f54-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="c5f54-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c5f54-110"><strong>Nome da exportação de importação salva</strong></span><span class="sxs-lookup"><span data-stu-id="c5f54-110"><strong>Saved Import Export Name</strong></span></span></p></td>
<td><p><span data-ttu-id="c5f54-111">Selecione o nome de uma especificação de importação ou exportação salva, na lista suspensa.</span><span class="sxs-lookup"><span data-stu-id="c5f54-111">Select the name of a saved import or export specification from the drop-down list.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="c5f54-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="c5f54-112">Remarks</span></span>

- <span data-ttu-id="c5f54-113">Esta macro tem o mesmo efeito deste procedimento quando executado no Access:</span><span class="sxs-lookup"><span data-stu-id="c5f54-113">This macro action has the same effect as performing the following procedure in Access:</span></span>
    
  1.  <span data-ttu-id="c5f54-114">Na guia **Dados Externos**, clique em **Importações Salvas** ou em **Exportações Salvas**.</span><span class="sxs-lookup"><span data-stu-id="c5f54-114">On the **External Data** tab, click either **Saved Imports** or **Saved Exports**.</span></span>
    
  2.  <span data-ttu-id="c5f54-115">Na caixa de diálogo **Gerenciar Tarefas de Dados**, na guia **Importações Salvas** ou **Exportações Salvas** (dependendo da sua escolha na etapa anterior), clique na especificação a ser executada.</span><span class="sxs-lookup"><span data-stu-id="c5f54-115">In the **Manage Data Tasks** dialog box, on the **Saved Imports** or **Saved Exports** tab (depending on your choice in the preceding step), click the specification that you want to run.</span></span>
    
  3.  <span data-ttu-id="c5f54-116">Clique em **Executar**.</span><span class="sxs-lookup"><span data-stu-id="c5f54-116">Click **Run**.</span></span>

- <span data-ttu-id="c5f54-117">Antes de executar a ação **ExecutarImportaçãoOuExportaçãoSalva**, verifique se os arquivos de origem e de destino existem, se os dados de origem estão prontos para a importação e se a operação não substituirá acidentalmente nenhum dado do arquivo de destino.</span><span class="sxs-lookup"><span data-stu-id="c5f54-117">Before running the **RunSavedImportExport** action, make sure that the source and destination files exist, the source data is ready for importing, and that the operation will not accidentally overwrite any data in your destination file.</span></span>

- <span data-ttu-id="c5f54-118">Na seção **Consulte Também**, localize links para obter mais informações sobre como salvar e executar especificações de importação e exportação.</span><span class="sxs-lookup"><span data-stu-id="c5f54-118">Find links to more information about saving and running import and export specifications in the **See Also** section.</span></span>

- <span data-ttu-id="c5f54-119">Se a especificação salva de  importação ou exportação escolhida para o argumento Nome da Exportação de Importação Salva for excluída depois que a macro for criada, o Access exibirá a seguinte mensagem de erro quando a macro for executado: A especificação com o índice especificado não **existe. Especifique um índice diferente. '\*\*\*\*\*nome da especificação\*\*\*\*\*'.**</span><span class="sxs-lookup"><span data-stu-id="c5f54-119">If the saved import or export specification you choose for the **Saved Import Export Name** argument is deleted after the macro is created, Access displays the following error message when the macro is run: **The specification with the specified index does not exist. Specify a different index. '\*\*\*\*\*specification name\*\*\*\*\*'.**</span></span>

