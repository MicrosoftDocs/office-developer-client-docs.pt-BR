---
title: Usando o ADO for Internet Publishing
TOCTitle: Using ADO for Internet Publishing
ms:assetid: 1e829783-fc12-e303-6f12-2df1ca96cb0f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248975(v=office.15)
ms:contentKeyID: 48543622
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 22f89b4fb22e7625f73eb938aa011beb42c6b99c
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944344"
---
# <a name="using-ado-for-internet-publishing"></a>Usando o ADO for Internet publishing


**Aplica-se a**: Access 2013, o Office 2013



[O OLE DB Provider for Internet Publishing](the-ole-db-provider-for-internet-publishing.md) mostra um exemplo específico de acesso a dados heterogêneos com o ADO. Embora os exemplos desta seção sejam específicos ao uso do Internet Publishing Provider, os princípios demonstrados devem ser semelhantes na utilização do ADO com outros provedores para dados heterogêneos, como um provedor para repositório de emails.

## <a name="urls"></a>URLs

As URLs podem ser usadas como uma alternativa para as sequências de conexão e o texto de comando a fim de especificar fontes de dados e o local de arquivos e diretórios. Você pode utilizá-las com os objetos [Connection](connection-object-ado.md) e **Recordset** existentes, e também com os objetos **Record** e **Stream**.

Para obter mais informações sobre como usar URLs, consulte [URLs absolutas e relativas](absolute-and-relative-urls.md).

## <a name="record-fields"></a>Campos de registro

A diferença entre dados heterogêneos e dados homogêneos é que para o primeiro, cada linha de dados, ou **Registro**, pode ter um conjunto diferente de colunas, ou **Campos**. No caso dos dados homogêneos, cada linha possui o mesmo conjunto de colunas. Para obter mais informações sobre os campos específicos do Internet Publishing Provider, consulte [Registros e campos extras fornecidos pelo provedor](records-and-provider-supplied-fields.md).

## <a name="appending-new-fields"></a>Acrescentando novos campos

Vários objetos ADO foram aprimorados para funcionar junto com objetos **Record** e **Stream**.

  - O método [Append](fields-collection-ado.md) da coleção [Fields](append-method-ado.md), que cria e adiciona um objeto [Field](field-object-ado.md) à coleção, também pode especificar o valor de **Field**.

  - O método [Update](update-method-ado.md) finaliza a adição ou a exclusão de campos da coleção.

  - Como atalho e alternativa ao método **Append**, você pode criar campos simplesmente atribuindo um valor a um campo indefinido ou excluído anteriormente.

## <a name="see-also"></a>Confira também

- [Tópicos de cenário de publicação na Internet](internet-publishing-scenario.md)