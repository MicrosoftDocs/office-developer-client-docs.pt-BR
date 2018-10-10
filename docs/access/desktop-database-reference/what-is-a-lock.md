---
title: O que é um bloqueio? (Referência de banco de dados da área de trabalho do access)
TOCTitle: What is a Lock?
ms:assetid: 9ddc3198-1531-1d8f-153d-fc79847e388a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249721(v=office.15)
ms:contentKeyID: 48546636
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f852901be41060568bdbad539906e9166d080fad
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463816"
---
# <a name="what-is-a-lock"></a>O que é um bloqueio?


**Aplica-se a**: Access 2013 | Office 2013

Bloqueio é o processo pelo qual um DBMS restringe o acesso a uma linha em um ambiente com vários usuários. Quando uma linha ou coluna é bloqueada exclusivamente, outros usuários não têm permissão para acessar os dados bloqueados até que o bloqueio seja liberado. Isso garante que dois usuários não possam atualizar a mesma coluna simultaneamente em uma linha.

Os bloqueios podem ser muito onerosos a partir de uma perspectiva do recurso e deveria ser usada apenas quando necessário para preservar a integridade dos dados. Em um banco de dados no qual centenas ou milhares de usuários poderiam estar tentando acessar um registro a cada segundo  como um banco de dados conectado à Internet  o bloqueio desnecessário poderia resultar rapidamente em um desempenho mais lento no seu aplicativo.

Você pode controlar como a fonte de dados e a biblioteca de cursor ADO gerenciam a concorrência, escolhendo a opção de bloqueio adequada.

Defina a propriedade **LockType** antes de abrir um **Recordset** para especificar qual tipo de bloqueio o provedor deveria usar ao abri-lo. Leia a propriedades para retornar o tipo de bloqueio em uso em um objeto **Recordset** aberto.

Os provedores não podem oferecer suporte a todos os tipos de bloqueio. Se um provedor não puder oferecer suporte à configuração **LockType** solicitada, ele substituirá outro tipo de bloqueio. Para determinar a funcionalidade de bloqueio real disponível em um objeto **Recordset**, use o método [Supports](supports-method-ado.md) com **adUpdate** e **adUpdateBatch**.

Não há suporte para a configuração **adLockPessimistic** se a propriedade [CursorLocation](cursorlocation-property-ado.md) for definida como **adUseClient**. Se um valor sem suporte for definido, nenhum erro ocorrerá; o **LockType** suportado mais próximo será usado.

A propriedade **LockType** é de leitura/gravação quando o **Recordset** está fechado e somente leitura quando está aberto.

