---
title: 'Capítulo 6: Tratamento de erros'
TOCTitle: 'Chapter 6: Error handling'
ms:assetid: 6ae7343b-b9e0-c4c3-f65c-110f903e573e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249420(v=office.15)
ms:contentKeyID: 48545440
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 14d3dc4b291d96a47e0fb67c0e7d837463cd4bf2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296406"
---
# <a name="chapter-6-error-handling"></a>Capítulo 6: Tratamento de erros

**Aplica-se ao:** Access 2013, Office 2013

O ADO usa vários métodos para notificar um aplicativo sobre os erros ocorridos. Este capítulo aborda os tipos de erros que podem ocorrer quando você usa o ADO e como seu aplicativo é notificado. No final, ele apresenta sugestões sobre como tratar esses erros.

## <a name="how-does-ado-report-errors"></a>Como o ADO relata erros?

O ADO notifica-o sobre erros de diversas maneiras:

- Os erros do ADO geram um erro de tempo de execução. Trate um erro do ADO da mesma maneira que trataria qualquer outro erro de tempo de execução como, por exemplo, usando uma instrução **On Error** do Visual Basic.

- Seu programa pode receber erros do OLE DB. Um erro do OLE DB também gera um erro de tempo de execução.

- Se o erro for específico do provedor de dados, um ou mais objetos **Error** serão incluídos na coleção **Errors** do objeto **Connection** que foi usado para acessar o repositório de dados quando o erro ocorreu.

- Se o processo que gerou um evento também produziu um erro, as informações sobre o erro serão incluídas em um objeto **Error** e passadas como um parâmetro para o evento. Consulte o [Capítulo 7: Tratando eventos do ADO](chapter-7-handling-ado-events.md) para obter mais informações sobre eventos.

- Os problemas que ocorrem durante o processamento de atualizações em lotes ou outras operações em massa que envolvem um **Recordset** podem ser indicados pela propriedade **Status** do **Recordset**. Por exemplo, violações de restrições de esquema ou permissões insuficientes podem ser especificadas por valores **RecordStatusEnum**.

- Os problemas ocorridos que envolvem um **Field** específico no registro atual também são indicados pela propriedade **Status** de cada **Field** na coleção **Fields** do **Record** ou **Recordset**. Por exemplo, as atualizações que não puderam ser concluídas ou os tipos de dados incompatíveis podem ser especificados por valores **FieldStatusEnum**.

As seções a seguir descrevem cada um desses métodos de notificação em mais detalhes.

- [Erros do ADO](ado-errors.md)
- [Referência de erros do ADO](ado-error-reference.md)
- [Erros do provedor](provider-errors.md)
- [Informações de erro relacionado ao campo](field-related-error-information.md)
- [Informações de erro relacionado ao conjunto de registros](recordset-related-error-information.md)
- [Antecipação de erros](anticipating-errors.md)
- [Tratamento de erros em outros idiomas (ADO)](handling-errors-in-other-languages.md)
