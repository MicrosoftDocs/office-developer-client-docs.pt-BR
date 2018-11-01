---
title: Adicionando registros (referência de banco de dados da área de trabalho do Access)
TOCTitle: Adding Records
ms:assetid: 7a5b27bc-7b28-4f43-b55e-a21edfb9e1b3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249505(v=office.15)
ms:contentKeyID: 48545791
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 760c9b2915b84457d64325c97c5118fb5debc925
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880590"
---
# <a name="adding-records"></a>Adição de registros


**Aplica-se a**: Access 2013, o Office 2013

Use o método **AddNew** para criar e inicializar um novo registro em um **Recordset**. Você pode usar o método **Supports** com o valor **CursorOptionEnum** **adAddNew** para verificar se é possível adicionar registros ao objeto **Recordset** atual.

Depois que você chamar o método **AddNew**, o novo registro se tornará o registro atual e permanecerá atual até a chamada do método **Update**. Se o objeto **Recordset** não oferecer suporte a indicadores, pode ser que você não consiga acessar o novo registro se passar para outro. Assim, dependendo do tipo de cursor, talvez seja necessário chamar o método **Requery** para tornar o novo registro acessível.

Se você chamar **AddNew** durante a edição do registro atual ou a adição de um novo registro, o ADO chamará o método **Update** para salvar as alterações e, em seguida, criará o novo registro.

Esta seção inclui os seguintes tópicos:

- [Adição de vários campos](adding-multiple-fields.md)

- [Determinação do modo de edição](determining-edit-mode.md)

- [Usando AddNew nos Modos de atualização imediata e em lotes](using-addnew-in-immediate-and-batch-modes.md)

