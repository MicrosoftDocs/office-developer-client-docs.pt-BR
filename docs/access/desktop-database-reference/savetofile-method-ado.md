---
title: Método SaveToFile (ADO)
TOCTitle: SaveToFile method (ADO)
ms:assetid: db0fd95e-8ef3-af87-5346-8f8713153ca7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250104(v=office.15)
ms:contentKeyID: 48548097
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f3b08c9df435c7ce995a40af7b8ad5466b79245d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308922"
---
# <a name="savetofile-method-ado"></a>Método SaveToFile (ADO)

**Aplica-se ao:** Access 2013, Office 2013

Salva o conteúdo binário de um [Stream](stream-object-ado.md) para um arquivo.

## <a name="syntax"></a>Sintaxe

*Stream*. SaveToFile *FileName*, *SaveOptions*

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*FileName* |Um valor **String** que contém o nome totalmente qualificado do arquivo no qual o conteúdo do **Stream** será salvo. É possível salvar em qualquer localidade local válida ou em qualquer local que você tenha acesso por um valor de UNC.|
|*SaveOptions* |Um valor [SaveOptionsEnum](saveoptionsenum.md) que especifica se um novo arquivo deve ser criado por **SaveToFile**, se ele ainda não existir. O valor padrão é **adSaveCreateNotExists**. Com essas opções, é possível especificar que ocorre um erro se o arquivo especificado não existir. Também é possível especificar se **SaveToFile** sobrescreve o conteúdo atual de um arquivo existente.|

> [!NOTE]
> [!OBSERVAçãO] Se você sobrescrever um arquivo existente (quando **adSaveCreateOverwrite** estiver definido), **SaveToFile** truncará quaisquer bytes do arquivo existente original que seguem o novo [EOS](eos-property-ado.md).

## <a name="remarks"></a>Comentários

**SaveToFile** pode ser utilizado para copiar o conteúdo de um objeto **Stream** para um arquivo local. Não há alteração no conteúdo ou nas propriedades do objeto **Stream**. O objeto **Stream** deve estar aberto antes de chamar **SaveToFile**.

Este método não altera a associação do objeto **Stream** com sua fonte base. O objeto **Stream** ainda estará associado à URL original ou ao **Record** que era sua fonte quando foi aberto.

Após uma operação **SaveToFile**, a posição atual ([Position](position-property-ado.md)) no fluxo será definida para o início do fluxo (0).

