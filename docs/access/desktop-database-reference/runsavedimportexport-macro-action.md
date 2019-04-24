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
# <a name="runsavedimportexport-macro-action"></a>Ação da macro ExecutarImportaçãoOuExportaçãoSalva

**Aplica-se ao:** Access 2013, Office 2013

Você pode usar a ação **ExecutarImportaçãoOuExportaçãoSalva** para executar uma especificação de importação ou exportação salva e criada com o Assistente de Importação ou com o Assistente de Exportação.

> [!NOTE]
> [!OBSERVAçãO] This action will not be allowed if the database is not trusted.

## <a name="setting"></a>Configuração

A ação **ExecutarImportaçãoOuExportaçãoSalva** tem o argumento a seguir.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento da ação</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Nome da exportação de importação salva</strong></p></td>
<td><p>Selecione o nome de uma especificação de importação ou exportação salva, na lista suspensa.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

- Esta macro tem o mesmo efeito deste procedimento quando executado no Access:
    
  1.  Na guia **Dados Externos**, clique em **Importações Salvas** ou em **Exportações Salvas**.
    
  2.  Na caixa de diálogo **Gerenciar Tarefas de Dados**, na guia **Importações Salvas** ou **Exportações Salvas** (dependendo da sua escolha na etapa anterior), clique na especificação a ser executada.
    
  3.  Clique em **Executar**.

- Antes de executar a ação **ExecutarImportaçãoOuExportaçãoSalva**, verifique se os arquivos de origem e de destino existem, se os dados de origem estão prontos para a importação e se a operação não substituirá acidentalmente nenhum dado do arquivo de destino.

- Na seção **Consulte Também**, localize links para obter mais informações sobre como salvar e executar especificações de importação e exportação.

- Se a especificação de importação ou exportação salva que você escolher para o argumento **Saved Import Export Name** for excluída após a criação da macro, o Access exibirá a seguinte mensagem de erro quando a macro for executada: **a especificação com o índice especificado faz Não existe. Especifique um índice diferente. ' * * * * * nome da especificação [* * * * '.**

