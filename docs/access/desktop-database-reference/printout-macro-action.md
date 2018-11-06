---
title: Ação da macro Imprimir
TOCTitle: PrintOut macro action
ms:assetid: 13688158-1cf1-4b2e-d90a-271c8890e413
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845432(v=office.15)
ms:contentKeyID: 48543368
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm1697
f1_categories:
- Office.Version=v15
ms.openlocfilehash: c2e5b3e2cdfb743df8a098d3978ccd3d6eb66d90
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25999026"
---
# <a name="printout-macro-action"></a>Ação da macro Imprimir

**Aplica-se a**: Access 2013, o Office 2013

Você pode usar a ação **Imprimir** para imprimir o objeto ativo no banco de dados aberto. Pode imprimir folhas de dados, relatórios, formulários, páginas de acesso a dados e módulos.

> [!NOTE]
> [!OBSERVAçãO] This action will not be allowed if the database is not trusted. 

## <a name="setting"></a>Configuração

A ação **Imprimir** tem os seguintes argumentos.

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
<td><p><strong>Intervalo de Impressão</strong></p></td>
<td><p>O intervalo da impressão. Clique em <strong>Tudo</strong> (o usuário pode imprimir todo o objeto), <strong>Seleção</strong> (o usuário pode imprimir parte do objeto selecionado) ou <strong>Páginas</strong> (o usuário pode especificar um intervalo de páginas nos argumentos <strong>Da Página</strong> e <strong>À Página</strong>) na caixa <strong>Intervalo de Impressão</strong> da seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros. O padrão é <strong>Tudo</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Da Página</strong></p></td>
<td><p>A primeira página que será impressa. A impressão começa na parte superior dessa página. Este argumento é obrigatório para selecionar <strong>Páginas</strong> na caixa <strong>Intervalo de Impressão</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>À Página</strong></p></td>
<td><p>A última página que será impressa. A impressão para na parte inferior dessa página. Este argumento é obrigatório para selecionar <strong>Páginas</strong> na caixa <strong>Intervalo de Impressão</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Qualidade de Impressão</strong></p></td>
<td><p>A qualidade de impressão. Clique em <strong>Alta</strong>, <strong>Média</strong>, <strong>Baixa</strong> ou <strong>Rascunho</strong>. Quanto menor for a qualidade, mais rapidamente o objeto será impresso. O padrão é <strong>Alta</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Copies</strong></p></td>
<td><p>O número de cópias que serão impressas. O padrão é 1.</p></td>
</tr>
<tr class="even">
<td><p><strong>Agrupar Cópias</strong></p></td>
<td><p>Clique em <strong>Sim</strong> (agrupar as cópias impressas) ou <strong>Não</strong> (não agrupar as cópias). O objeto poderá ser impresso com mais rapidez se este argumento for definido como <strong>Não</strong>. O padrão é <strong>Sim</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Esta ação é semelhante a selecionar um objeto, clicar na guia **Arquivo** e clicar em **Imprimir**. Com esta ação, porém, não é exibida nenhuma caixa de diálogo **Imprimir**.

> [!TIP]
> [!DICA] Se houver configurações de impressão específicas usadas com frequência, crie uma macro que contém a ação **Imprimir** com essas configurações nos argumentos.

Os argumentos desta ação correspondem às opções da caixa de diálogo **Imprimir**. Entretanto, diferentemente da ação **EncontrarRegistro** e **Localizar e Substituir**, as configurações do argumento não são compartilhadas com as opções da caixa de diálogo **Imprimir**.

Para executar a ação **Imprimir** em um módulo do VBA (Visual Basic for Applications), use o método **PrintOut** do objeto **DoCmd**.

