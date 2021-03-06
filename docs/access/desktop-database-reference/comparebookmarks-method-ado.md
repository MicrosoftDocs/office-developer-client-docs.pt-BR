---
title: Método CompareBookmarks (ADO)
TOCTitle: CompareBookmarks method (ADO)
ms:assetid: 826cb3c7-2f5c-284f-421d-6b7b07f14dec
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249564(v=office.15)
ms:contentKeyID: 48545977
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 460a77284141daad1834699c4dc1775be05c5c26
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296091"
---
# <a name="comparebookmarks-method-ado"></a>Método CompareBookmarks (ADO)

**Aplica-se ao:** Access 2013, Office 2013

Compara dois indicadores e retorna uma indicação de seus valores relativos.

## <a name="syntax"></a>Sintaxe

*result*  =  *recordset*. CompareBookmarks(*Bookmark1*, *Bookmark2*)

## <a name="return-value"></a>Valor de retorno

Retorna um valor [CompareEnum](compareenum.md) que indica a posição de linha relativa de dois registros representados por seus indicadores.

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*Bookmark1* |O indicador da primeira linha.|
|*Bookmark2* |O indicador da segunda linha.|

## <a name="remarks"></a>Comentários

Os indicadores devem ser aplicados ao mesmo objeto [Recordset](recordset-object-ado.md), ou a um objeto **Recordset** e seu [clone](clone-method-ado.md). Não é possível comparar com segurança indicadores de objetos **Recordset** diferentes, mesmo se eles foram criados a partir da mesma fonte ou comando. Também não é possível comparar indicadores para um objeto **Recordset** cujo provedor base não suporte comparações.

Um indicador identifica exclusivamente uma linha em um objeto **Recordset**. Utilize a propriedade [Bookmark](bookmark-property-ado.md) da linha atual para obter seu indicador.

Como o tipo de dados de um indicador é específico do provedor, o ADO o expõe como uma Variant. Por exemplo, os indicadores do SQL Server são do tipo DBTYPE \_ R8 (Double). O ADO exporá esse tipo como uma Variant com um subtipo igual a Double.

Ao comparar indicadores, o ADO não tenta nenhum tipo de imposição. Os valores são simplesmente passados para o provedor onde a comparação ocorre. Se os indicadores passados para o método **CompareBookmarks** forem armazenados em variáveis de tipos diferentes, ele pode gerar o erro de tipos incompatíveis "Os argumentos são do tipo errado, estão fora do intervalo aceitável ou estão em conflito entre si."

Um indicador que não seja válido ou esteja formado incorretamente causará um erro.

