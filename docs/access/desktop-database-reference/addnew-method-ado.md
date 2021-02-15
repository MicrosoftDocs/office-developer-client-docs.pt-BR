---
title: Método AddNew (ADO)
TOCTitle: AddNew method (ADO)
ms:assetid: bae09be0-5707-4f38-9c74-0acd0f29dbac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249899(v=office.15)
ms:contentKeyID: 48547384
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f733c574ba7927587c6fcb6305a361ca1070de0f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282510"
---
# <a name="addnew-method-ado"></a>Método AddNew (ADO)

**Aplica-se ao:** Access 2013, Office 2013

Cria um novo registro para um objeto [Recordset](recordset-object-ado.md) atualizável.

## <a name="syntax"></a>Sintaxe

*recordset*. AddNew *FieldList*, *Values*

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*recordset* |Um objeto **Recordset**.|
|*FieldList* |Opcional. Um único nome, ou uma matriz de nomes ou posições ordinais dos campos no novo registro.|
|*Values* |Opcional. Um único valor, ou uma matriz de valores para os campos no novo registro. Se *Fieldlist* for uma matriz, *Values* também deverá ser uma matriz com o mesmo número de membros; caso contrário, ocorrerá erro. A ordem dos nomes de campo deve corresponder à ordem dos valores de campo em cada matriz.|

## <a name="remarks"></a>Comentários

Use o método **AddNew** para criar e inicializar um novo registro. Use o método [Supports](supports-method-ado.md) com **adAddNew** (valor [CursorOptionEnum](cursoroptionenum.md)) para verificar se é possível adicionar registros ao objeto **Recordset** atual.

Depois que você chamar o método **AddNew**, o novo registro passará a ser o registro atual e permanecerá atual depois que o método [Update](update-method-ado.md) for chamado. Como o novo registro é acrescentado a **Recordset**, uma chamada para **MoveNext** após Update ultrapassará o fim de **Recordset**, tornando **EOF** True. Se o objeto **Recordset** não oferecer suporte a indicadores, você não poderá acessar o novo registro ao passar para outro. Dependendo do tipo de cursor, talvez seja necessário chamar o método [Requery](requery-method-ado.md) para tornar o novo registro acessível.

Se você chamar **AddNew** durante a edição do registro atual ou a adição de um novo registro, o ADO chamará o método **Update** para salvar as alterações e, em seguida, criará o novo registro.

O comportamento do método **AddNew** depende do modo de atualização do objeto **Recordset** e se serão passados os argumentos *Fieldlist* e *Values*.

No *modo de atualização imediato* (em que o provedor grava as alterações na fonte de dados subjacente quando você chama o método **Update**), se você chamar o método **AddNew** sem argumentos, a propriedade [EditMode](editmode-property-ado.md) será definida como **adEditAdd** (valor [EditModeEnum](editmodeenum.md)). O provedor armazena localmente em cache qualquer alteração de valor de campo. A chamada do método **Update** posta o novo registro no banco de dados e redefine a propriedade **EditMode** como  **adEditNone** (valor **EditModeEnum**). Se você passar os argumentos *Fieldlist* e *Values*, o ADO postará o novo registro imediatamente no banco de dados (nenhuma chamada de **Update** é necessária); o valor da propriedade **EditMode** não é alterado (**adEditNone**).

No *modo de atualização em lotes* (em que o provedor armazena em cache várias alterações, gravando-as na fonte de dados subjacente somente quando o método [UpdateBatch](updatebatch-method-ado.md) é chamado), se você chamar o método **AddNew** sem argumentos, definirá a propriedade **EditMode** como **adEditAdd**. O provedor armazena localmente em cache qualquer alteração de valor de campo. A chamada do método **Update** adiciona o novo registro ao **Recordset** atual e redefine a propriedade **EditMode** como **adEditNone**, entretanto, o provedor não postará as alterações no banco de dados subjacente até que o método **UpdateBatch** seja chamado. Se você passar os argumentos *Fieldlist* e *Values*, o ADO enviará o novo registro para que o provedor o armazene em um cache; você precisará chamar o método **UpdateBatch** para postar o novo registro no banco de dados subjacente.

