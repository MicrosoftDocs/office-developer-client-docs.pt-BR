---
title: Método CopyTo (ADO)
TOCTitle: CopyTo method (ADO)
ms:assetid: 1c1ab950-51f7-7ecc-ccd8-e689db02f06a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248958(v=office.15)
ms:contentKeyID: 48543558
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2e8de2caf2abc53b0dbd014f21a85a6d54749033
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295475"
---
# <a name="copyto-method-ado"></a>Método CopyTo (ADO)

**Aplica-se ao:** Access 2013, Office 2013

Copia o número especificado de caracteres ou bytes (dependendo de [Type](type-property-ado-stream.md)) no [Stream](stream-object-ado.md) para outro objeto **Stream**.

## <a name="syntax"></a>Sintaxe

*Stream*. CopyTo *DestStream*, *NUMCHARS*

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*DestStream* |Um valor de variável de objeto que contém uma referência para um objeto **Stream** aberto. O **Stream** atual é copiado para o **Stream** de destino especificado por *DestStream*. O **Stream** de destino já deve estar aberto. Se não estiver, ocorrerá um erro em tempo de execução.<br/><br/>**Observação**: o parâmetro *DestStream* pode não ser um proxy do objeto **Stream** porque isso requer acesso a uma interface privada no objeto **Stream** que não pode ser remota ao cliente.|
|*NumChars* |Opcional. Um valor **Integer** que especifica o número de bytes ou caracteres a serem copiados da posição atual no **Stream** de origem para o **Stream** de destino. O valor padrão é –1, que especifica que todos os caracteres ou bytes são copiados da posição atual até o [EOS](eos-property-ado.md).|

## <a name="remarks"></a>Comentários

Este método copia o número especificado de caracteres ou bytes, iniciando na posição atual especificada pela propriedade [Position](position-property-ado.md). Se o número especificado for maior que o número de bytes disponíveis até o **EOS**, apenas os caracteres ou bytes a partir da posição atual até o **EOS** serão copiados. Se o valor de *NumChars* for –1 ou omitido, todos os caracteres ou bytes a partir da posição atual serão copiados.

Se houver caracteres ou bytes existentes no fluxo de destino, todo o conteúdo além do ponto em que a cópia termina permanecerá e não será truncado. **Position** se torna o byte que segue imediatamente o último byte copiado. Se você deseja truncar esses bytes, chame [SetEOS](seteos-method-ado.md).

**CopyTo** deve ser utilizado para copiar dados para um **Stream** de destino do mesmo tipo que o **Stream** de origem (as definições de sua propriedade **Type** são ambas **adTypeText** ou ambas **adTypeBinary**). Para objetos **Stream** de texto, é possível alterar a definição da propriedade [Charset](charset-property-ado.md) do **Stream** de destino para converter de um conjunto de caracteres para outro. Além disso, objetos **Stream** de texto podem ser copiados com êxito para objetos **Stream** binários, mas objetos **Stream** binários não podem ser copiados para objetos **Stream** de texto.

