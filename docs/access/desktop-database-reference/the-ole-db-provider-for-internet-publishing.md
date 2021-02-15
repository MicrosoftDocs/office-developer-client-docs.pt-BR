---
title: O OLE DB Provider for Internet Publishing
TOCTitle: The OLE DB Provider for Internet Publishing
ms:assetid: 864e5ece-0f50-5d88-4c40-f951b2a2eded
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249583(v=office.15)
ms:contentKeyID: 48546082
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 617dca5ced5410e2023657ea1b0b748066f7843f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314053"
---
# <a name="ole-db-provider-for-internet-publishing"></a>OLE DB Provider for Internet Publishing

**Aplica-se ao:** Access 2013, Office 2013

Os objetos [Record](record-object-ado.md) e [Stream](stream-object-ado.md) do ADO podem ser usados com o Microsoft OLE DB Provider for Internet Publishing (Internet Publishing Provider) para acessar e manipular recursos, como pastas da Web ou arquivos servidos pelo Microsoft FrontPage. Com o ADO, você pode especificar a origem de um **Record**, **Stream** ou [Recordset](recordset-object-ado.md) que será uma URL. Em seguida, você pode fazer upload, baixar, mover, copiar e excluir os recursos, ou manipular diretamente as propriedades de recursos.

Por exemplo, codifique usando **Records** e **Streams** com o Internet Publishing Provider, consulte o [Cenário de publicação na Internet](internet-publishing-scenario.md).

O Internet Publishing Provider é instalado com o Microsoft Windows 2000. As versões anteriores do Internet Publishing Provider também estão disponíveis com o Microsoft Office 2000 e o Microsoft Internet Explorer 5.0.

Há três maneiras de se conectar o ADO ao Internet Publishing Provider:

- Especifique "URL=" na sequência de conexão. Por exemplo:
    
  ```vb 
     
    objConn.Open "URL=https://servername" 
  ```

- Especifique Msdaipp.dso para a palavra-chave *Provider* da sequência de conexão. Por exemplo:
    
  ```vb 
     
    objConn.Open "provider=MSDAIPP.DSO;data source=https://servername" 
  ```

- Especifique Msdaipp.dso para a propriedade [Provider](provider-property-ado.md) do objeto [Connection](connection-object-ado.md). Por exemplo:
    
  ```vb 
     
    objConn.Provider = "MSDAIPP.DSO" 
    objConn.Open "https://servername" 
  ```

> [!NOTE]
> Se Msdaipp.dso for explicitamente especificado como o valor do provedor, com a palavra-chave de sequência de conexão *Provider* ou a propriedade **Provider**, você não poderá utilizar "URL=" na sequência de conexão. Se o fizer, ocorrerá um erro. Em vez disso, basta especificar a URL, conforme mostrado anteriormente neste tópico.

Para obter informações mais específicas sobre o Internet Publishing Provider, consulte [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) ou a documentação do provedor fornecida com o aplicativo de origem com o qual o OLE DB Provider for Internet Publishing foi instalado: Windows 2000, Office 2000 ou Internet Explorer 5.0.

