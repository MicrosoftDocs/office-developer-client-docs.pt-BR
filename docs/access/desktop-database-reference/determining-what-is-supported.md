---
title: Determinação do que é compatível
TOCTitle: Determining what is supported
ms:assetid: 47b44dc9-e0fd-f204-0c68-e0de9247ee2c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249221(v=office.15)
ms:contentKeyID: 48544602
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3abef84f05ad279edba1fcc753f0b412a807a7b9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293907"
---
# <a name="determining-what-is-supported"></a>Determinação do que é compatível

**Aplica-se ao:** Access 2013, Office 2013

O método **Supports** é usado para determinar se um objeto **Recordset** especificado oferece suporte para um determinado tipo de funcionalidade. A sua sintaxe é a seguinte:

`boolean = recordset.Supports( CursorOptions )`

**Supports** retorna um valor booleano que indica se todos os recursos identificados pelo argumento *CursorOptions* têm o suporte do provedor. Você pode usar o método **Supports** para determinar os tipos de funcionalidade para os quais um objeto **Recordset** oferece suporte. Se o objeto **Recordset** oferecer suporte para os recursos cujas constantes correspondentes estão em *CursorOptions*, o método **Supports** retornará **True**. Caso contrário, retornará **False**.

Usando o método **Supports**, você pode verificar a capacidade de o objeto **Recordset** adicionar novos registros, usar indicadores, usar o método **Find**, usar rolagem, usar a propriedade **Index** e executar atualizações em lotes. Para obter uma lista completa das constantes e de seus significados, consulte [CursorOptionEnum](cursoroptionenum.md).

Embora o método **Supports** possa retornar **True** para uma determinada funcionalidade, ele não garante que o provedor possa disponibilizar o recurso em todas as circunstâncias. O método **Supports** apenas retorna se o provedor pode oferecer suporte para a funcionalidade especificada, considerando que determinadas condições sejam atendidas. Por exemplo, o método **Supports** pode indicar que um objeto **Recordset** oferece suporte para atualizações, embora o cursor seja baseado em uma junção de várias tabelas  algumas colunas das quais não podem ser atualizadas.

