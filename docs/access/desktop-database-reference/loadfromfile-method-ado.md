---
title: Método loadFromfile (ADO)
TOCTitle: LoadFromFile method (ADO)
ms:assetid: 33fd543f-bd24-9199-7540-2889b69221c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249107(v=office.15)
ms:contentKeyID: 48544123
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9316bc4302a559fa44082a0576595707157e9d64
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289882"
---
# <a name="loadfromfile-method-ado"></a>Método loadFromfile (ADO)

**Aplica-se ao:** Access 2013, Office 2013

Carrega o conteúdo de um arquivo existente para dentro de um [Stream](stream-object-ado.md).

## <a name="syntax"></a>Sintaxe

*Stream*. *Nome de arquivo* LoadFromFile

## <a name="parameters"></a>Parâmetros

|Nome |Descrição|
|:----|:----------|
|*FileName* |Um valor **String** que contém o nome de um arquivo a ser carregado no **Stream**. *FileName* pode conter qualquer caminho e nome válidos em formato UNC. Se o arquivo especificado não existir, ocorrerá um erro em tempo de execução.|

## <a name="remarks"></a>Comentários

Este método pode ser utilizado para carregar o conteúdo de um arquivo local em um objeto **Stream**. Isso pode ser utilizado para fazer upload do conteúdo de um arquivo local para um servidor.

O objeto **Stream** já deve estar aberto antes de chamar **LoadFromFile**. Este método não altera a ligação do objeto **Stream**; ele ainda estará ligado ao objeto especificado pela URL ou **Record** com o qual o **Stream** foi originalmente aberto.

**LoadFromFile** sobrescreve o conteúdo atual do objeto **Stream** com os dados lidos do arquivo. Quaisquer bytes existentes no **Stream** serão sobrescritos pelo conteúdo do arquivo. Todos os bytes existentes anteriormente e remanescentes após o [EOS](eos-property-ado.md) criados por **LoadFromFile** são truncados.

Depois de uma chamada a **LoadFromFile**, a posição atual é definida para o início do **Stream** ([Position](position-property-ado.md) é 0).

Como 2 bytes podem ser adicionados no início do fluxo para codificação, o tamanho do fluxo pode não corresponder exatamente o tamanho do arquivo a partir do qual ele foi carregado.

