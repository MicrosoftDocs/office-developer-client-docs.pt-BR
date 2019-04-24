---
title: Coleção Fields (ADO)
TOCTitle: Fields collection (ADO)
ms:assetid: 029aa738-8726-54a6-1813-b152813948bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248791(v=office.15)
ms:contentKeyID: 48542962
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a537756483361733c087d5dc1c6bba6e649d17d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292570"
---
# <a name="fields-collection-ado"></a>Coleção Fields (ADO)


**Aplica-se ao:** Access 2013, Office 2013

Contém todos os objetos [Field](field-object-ado.md) de um objeto [Recordset](recordset-object-ado.md) ou [Record](record-object-ado.md).

## <a name="remarks"></a>Comentários

Um objeto **Recordset** tem uma coleção **Fields** composta de objetos **Field**. Cada objeto **Field** corresponde a uma coluna do **Recordset**. Preencha a coleção **Fields** antes de abrir o **Recordset** chamando o método [Refresh](refresh-method-ado.md) da coleção.

> [!NOTE]
> [!OBSERVAçãO] Consulte o tópico do objeto **Field** para obter uma explicação detalhada sobre como usar os objetos **Field**.

A coleção **Fields** tem um método [Append](append-method-ado.md), que cria e adiciona, de forma provisória, um objeto **Field** a uma coleção, e um método **Update**, que finaliza qualquer adição ou exclusão.

Um objeto **Record** que tem dois campos especiais que podem ser indexados com constantes [FieldEnum](fieldenum.md). Uma constante acessa um campo que contém o fluxo padrão do **Record** e a outra que acessa um campo que contém uma sequência URL absoluta para o **Record**.

Determinados provedores (por exemplo, o [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)) podem preencher a coleção **Fields** com um subconjunto de campos disponíveis para o **Record** ou **Recordset**. Outros campos não serão adicionados à coleção até que sejam mencionados primeiro pelo nome ou indexados pelo código.

Caso você tente mencionar um campo não existente pelo nome, um novo objeto **Field** será anexado à coleção **Fields** com um [Status](status-property-ado-field.md) de **adFieldPendingInsert**. Quando você chamar [Update](update-method-ado.md), o ADO criará um novo campo na fonte de dados, se permitido pelo provedor.

