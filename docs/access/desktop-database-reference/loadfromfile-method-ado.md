---
title: Método LoadFromFile (ADO)
TOCTitle: LoadFromFile Method (ADO)
ms:assetid: 33fd543f-bd24-9199-7540-2889b69221c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249107(v=office.15)
ms:contentKeyID: 48544123
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 61244e989815d5c4ba1943e61aea7f6a6abf139d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872029"
---
# <a name="loadfromfile-method-ado"></a>Método LoadFromFile (ADO)


**Aplica-se a**: Access 2013, o Office 2013



Carrega o conteúdo de um arquivo existente para dentro de um [Stream](stream-object-ado.md).

## <a name="syntax"></a>Sintaxe

*Stream*. LoadFromFile *FileName*

## <a name="parameter"></a>Parâmetros

  - *FileName*

  - Um valor **String** que contém o nome de um arquivo a ser carregado no **Stream**. *FileName* pode conter qualquer caminho e nome válidos no formato UNC. Se o arquivo especificado não existir, ocorrerá um erro em tempo de execução.

## <a name="remarks"></a>Comentários

Este método pode ser utilizado para carregar o conteúdo de um arquivo local em um objeto **Stream**. Isso pode ser utilizado para fazer upload do conteúdo de um arquivo local para um servidor.

O objeto **Stream** já deve estar aberto antes de chamar **LoadFromFile**. Este método não altera a ligação do objeto **Stream**; ele ainda estará ligado ao objeto especificado pela URL ou **Record** com o qual o **Stream** foi originalmente aberto.

**LoadFromFile** sobrescreve o conteúdo atual do objeto **Stream** com os dados lidos do arquivo. Quaisquer bytes existentes no **Stream** serão sobrescritos pelo conteúdo do arquivo. Todos os bytes existentes anteriormente e remanescentes após o [EOS](eos-property-ado.md) criados por **LoadFromFile** são truncados.

Depois de uma chamada a **LoadFromFile**, a posição atual é definida para o início do **Stream** ([Position](position-property-ado.md) é 0).

Como 2 bytes podem ser adicionados no início do fluxo para codificação, o tamanho do fluxo pode não corresponder exatamente o tamanho do arquivo a partir do qual ele foi carregado.

