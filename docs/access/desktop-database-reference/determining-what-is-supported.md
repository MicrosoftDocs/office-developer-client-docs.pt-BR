---
title: Determinando o que é suportado
TOCTitle: Determining what is supported
ms:assetid: 47b44dc9-e0fd-f204-0c68-e0de9247ee2c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249221(v=office.15)
ms:contentKeyID: 48544602
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3b2db5fbdf0d85ee48b9dbc494ccce6022bfb165
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946584"
---
# <a name="determining-what-is-supported"></a>Determinando o que é suportado

**Aplica-se a**: Access 2013, o Office 2013

O método **Supports** é usado para determinar se um objeto **Recordset** especificado oferece suporte para um determinado tipo de funcionalidade. A sua sintaxe é a seguinte:

`boolean = recordset.Supports( CursorOptions )`

**Supports** retorna um valor booleano que indica se todos os recursos identificados pelo argumento *CursorOptions* têm o suporte do provedor. Você pode usar o método **Supports** para determinar os tipos de funcionalidade para os quais um objeto **Recordset** oferece suporte. Se o objeto **Recordset** oferecer suporte para os recursos cujas constantes correspondentes estão em *CursorOptions*, o método **Supports** retornará **True**. Caso contrário, retornará **False**.

Usando o método **Supports**, você pode verificar a capacidade de o objeto **Recordset** adicionar novos registros, usar indicadores, usar o método **Find**, usar rolagem, usar a propriedade **Index** e executar atualizações em lotes. Para obter uma lista completa das constantes e de seus significados, consulte [CursorOptionEnum](cursoroptionenum.md).

Embora o método **Supports** possa retornar **True** para uma determinada funcionalidade, ele não garante que o provedor possa disponibilizar o recurso em todas as circunstâncias. O método **Supports** apenas retorna se o provedor pode oferecer suporte para a funcionalidade especificada, considerando que determinadas condições sejam atendidas. Por exemplo, o método **Supports** pode indicar que um objeto **Recordset** oferece suporte para atualizações, embora o cursor seja baseado em uma junção de várias tabelas  algumas colunas das quais não podem ser atualizadas.

