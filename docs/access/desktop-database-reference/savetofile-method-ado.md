---
title: Método SaveToFile (ADO)
TOCTitle: SaveToFile Method (ADO)
ms:assetid: db0fd95e-8ef3-af87-5346-8f8713153ca7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250104(v=office.15)
ms:contentKeyID: 48548097
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c0bd915a4eb6405b7d5ddd4bfe42eb4a98f68b89
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462574"
---
# <a name="savetofile-method-ado"></a>Método SaveToFile (ADO)


**Aplica-se a**: Access 2013 | Office 2013



Salva o conteúdo binário de um [Stream](stream-object-ado.md) para um arquivo.

## <a name="syntax"></a>Sintaxe

*Stream*. SaveToFile*FileName*, *SaveOptions*

## <a name="parameters"></a>Parâmetros

  - *FileName*

  - Um valor **String** que contém o nome totalmente qualificado do arquivo no qual o conteúdo do **Stream** será salvo. É possível salvar em qualquer localidade local válida ou em qualquer local que você tenha acesso por um valor de UNC.

  - *SaveOptions*

  - Um valor [SaveOptionsEnum](saveoptionsenum.md) que especifica se um novo arquivo deve ser criado por **SaveToFile**, se ele ainda não existir. O valor padrão é **adSaveCreateNotExists**. Com essas opções, é possível especificar que ocorre um erro se o arquivo especificado não existir. Também é possível especificar se **SaveToFile** sobrescreve o conteúdo atual de um arquivo existente.


> [!NOTE]
> <P>[!OBSERVAçãO] Se você sobrescrever um arquivo existente (quando <STRONG>adSaveCreateOverwrite</STRONG> estiver definido), <STRONG>SaveToFile</STRONG> truncará quaisquer bytes do arquivo existente original que seguem o novo <A href="eos-property-ado.md">EOS</A>.</P>



## <a name="remarks"></a>Comentários

**SaveToFile** pode ser utilizado para copiar o conteúdo de um objeto **Stream** para um arquivo local. Não há alteração no conteúdo ou nas propriedades do objeto **Stream**. O objeto **Stream** deve estar aberto antes de chamar **SaveToFile**.

Este método não altera a associação do objeto **Stream** com sua fonte base. O objeto **Stream** ainda estará associado à URL original ou ao **Record** que era sua fonte quando foi aberto.

Após uma operação **SaveToFile**, a posição atual ([Position](position-property-ado.md)) no fluxo será definida para o início do fluxo (0).
