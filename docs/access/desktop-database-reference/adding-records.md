---
title: Adicionando registros (referência de banco de dados da área de trabalho do Access)
TOCTitle: Adding Records
ms:assetid: 7a5b27bc-7b28-4f43-b55e-a21edfb9e1b3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249505(v=office.15)
ms:contentKeyID: 48545791
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bfa1503e7f7b874136ab5aee70721a3b9cf3463b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464916"
---
# <a name="adding-records"></a>Adicionando registros


**Aplica-se a**: Access 2013 | Office 2013

Use o método **AddNew** para criar e inicializar um novo registro em um **Recordset**. Você pode usar o método **Supports** com o valor **CursorOptionEnum** **adAddNew** para verificar se é possível adicionar registros ao objeto **Recordset** atual.

Depois que você chamar o método **AddNew**, o novo registro se tornará o registro atual e permanecerá atual até a chamada do método **Update**. Se o objeto **Recordset** não oferecer suporte a indicadores, pode ser que você não consiga acessar o novo registro se passar para outro. Assim, dependendo do tipo de cursor, talvez seja necessário chamar o método **Requery** para tornar o novo registro acessível.

Se você chamar **AddNew** durante a edição do registro atual ou a adição de um novo registro, o ADO chamará o método **Update** para salvar as alterações e, em seguida, criará o novo registro.

