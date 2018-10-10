---
title: 'Capítulo 10: Records e Streams'
TOCTitle: 'Chapter 10: Records and Streams'
ms:assetid: 74862096-2273-3b61-f89c-06554ccf42cd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249477(v=office.15)
ms:contentKeyID: 48545663
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4cdc7bbbaad7242ddbe2c4992395e6c4e0477504
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463585"
---
# <a name="chapter-10-records-and-streams"></a>Capítulo 10: Records e Streams


**Aplica-se a**: Access 2013 | Office 2013

O ADO atualmente fornece o objeto [Recordset](recordset-object-ado.md) como o principal meio de acessar informações nas fontes de dados, como bancos de dados relacionais. Entretanto, alguns provedores oferecem suporte a objetos [Record](record-object-ado.md) e [Stream](stream-object-ado.md) como objetos alternativos ou complementares com os quais os dados de provedores podem ser manipulados. Para obter especificações sobre o comportamento de **Record**, consulte a documentação do provedor.

## <a name="records"></a>Records

Os objetos **Record** funcionam essencialmente como um **Recordset** de uma linha. Entretanto, **Records** têm funções limitadas em comparação ao **Recordsets** e têm diferentes propriedades e métodos. A fonte para os dados no objeto **Record** pode ser um comando que retorne uma linha de dados do provedor. A utilização de objetos **Record** em vez de objetos **Recordset** para receber os resultados de uma consulta que retorne uma linha de dados elimina a sobrecarga de instanciação de um objeto **Recordset** mais complexo.

Os objetos **Record** podem servir para outro propósito, particularmente com os provedores de fontes de dados diferentes de bancos de dados relacionais tradicionais, como o [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). Muitas das informações que devem ser processadas existem não como tabelas nos bancos de dados, mas como mensagens em sistemas de email e como arquivos em sistemas de arquivo modernos. Os objetos **Record** e **Stream** facilitam o acesso às informações armazenadas em fontes diferentes de bancos de dados relacionais.

O objeto **Record** pode representar e gerenciar dados, como diretórios e arquivos, em um sistema de arquivos, ou pastas e mensagens em um sistema de email. Para esses propósitos, a fonte para **Record** pode ser a linha atual de um **Recordset** aberto, uma URL absoluta ou uma URL relativa em conjunto com um objeto [Connection](connection-object-ado.md) aberto.

Normalmente, um **Recordset** pode ser utilizado para representar um contêiner ou um pai na hierarquia, como uma pasta ou diretório. Um **Record** pode ser usado para retornar informações específicas sobre um nó no contêiner pai, como um arquivo ou documento. A principal razão para que os **Records** sejam utilizados para representar esse tipo de informação é que essas fontes de dados são heterogêneas. Isso significa que cada **Record** pode ter um conjunto e um número diferente de campos. Os **Recordsets** tradicionais que contêm linhas de um banco de dados são homogêneos, o que significa que cada linha tem o mesmo número e tipo de campos.

Para obter mais informações sobre a utilização do objeto **Record** para o processamento desses dados heterogêneos do provedor, como o Internet Publishing Provider, consulte [Usando o ADO for Internet Publishing](using-ado-for-internet-publishing.md).

## <a name="streams"></a>Streams

O objeto **Stream** fornece os meios para ler, escrever e gerenciar um fluxo de bytes. Esse fluxo de bytes pode ser texto ou um binário e está limitado em tamanho apenas por recursos de sistema. Em geral, os objetos **Stream** do ADO são utilizados com os seguintes propósitos:

  - Para conter o texto ou os bytes que compõem um arquivo ou uma mensagem, normalmente usado com provedores como o Microsoft OLE DB Provider for Internet Publishing. Para obter mais informações sobre esse uso dos objetos **Stream**, consulte [Usando o ADO for Internet Publishing](using-ado-for-internet-publishing.md).

Um objeto **Stream** pode ser aberto em:

  - Um arquivo simples especificado como uma URL.

  - Um campo de um **Record** ou um **Recordset** contendo um objeto **Stream**.

  - Um fluxo padrão de um objeto **Record** ou **Recordset** representando um diretório ou arquivo composto.

  - Um campo de recursos contendo a URL de um arquivo simples.

  - Nenhuma fonte em particular. Nesse caso, um objeto **Stream** é aberto na memória. Os dados podem ser escritos nele e salvos em outros **Stream** ou arquivo.

  - Um campo BLOB em um **Recordset**.

