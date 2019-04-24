---
title: Usando o ADO for Internet Publishing
TOCTitle: Using ADO for Internet Publishing
ms:assetid: 1e829783-fc12-e303-6f12-2df1ca96cb0f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248975(v=office.15)
ms:contentKeyID: 48543622
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ae8341151c7bf7d90585794061647ba33a5c4ea7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305898"
---
# <a name="using-ado-for-internet-publishing"></a>Uso do ADO para Publicação de Internet


**Aplica-se ao:** Access 2013, Office 2013



[O OLE DB Provider for Internet Publishing](the-ole-db-provider-for-internet-publishing.md) mostra um exemplo específico de acesso a dados heterogêneos com o ADO. Enquanto os exemplos nesta seção serão específicos para usar o provedor de publicação na Internet, os princípios demonstrados devem ser semelhantes ao usar o ADO com outros provedores para dados heterogêneos, como um provedor para um repositório de email.

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

- [Tópicos do cenário de publicação na Internet](internet-publishing-scenario.md)
