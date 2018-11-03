---
title: A família ADO das bibliotecas
TOCTitle: The ADO family of libraries
ms:assetid: 9e794509-d0a8-2e5b-02a8-65e26f059c4e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249724(v=office.15)
ms:contentKeyID: 48546656
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e4d37ef012e6db60c4a92267c82664694ed63afe
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936508"
---
# <a name="the-ado-family-of-libraries"></a>A família ADO das bibliotecas

**Aplica-se a**: Access 2013, o Office 2013

Três bibliotecas principais compõem a família ADO: ADO (incluindo RDS), ADO MD e ADOX.

## <a name="ado"></a>ADO

O ADO permite que os aplicativos clientes acessem e manipulem dados de um servidor de banco de dados através de um provedor OLE DB. Os principais benefícios do ADO são a facilidade de uso, a alta velocidade, baixa sobrecarga de memória e uma pequena superfície do disco. O ADO oferece suporte para os principais recursos de criação de aplicativos cliente/servidor e baseados na Web.

ADO também recursos Remote Data Service (RDS), ao qual você pode mover dados de um servidor a um aplicativo cliente ou página da Web, manipular os dados no cliente e retornar as atualizações para o servidor em uma única viagem de ida e.

## <a name="ado-md"></a>ADO MD

O Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) fornece acesso fácil aos dados multidimensionais de linguagens como Microsoft Visual Basic, Microsoft Visual C++ e Microsoft Visual J++. O ADO MD estende o ADO para incluir objetos específicos para dados multidimensionais, como os objetos **CubeDef** e **Cellset**. Com o ADO MD, é possível procurar esquema multidimensional, consultar um cubo e recuperar os resultados.

Assim como o ADO, o ADO MD usa um provedor OLE DB subjacente para obter acesso aos dados. Para trabalhar com o ADO MD, o provedor deve ser um MDP (provedor de dados multidimensionais), conforme definido pela especificação do OLE DB para OLAP. Os MDPs apresentam os dados em modos de exibição multidimensionais, ao contrário dos TDPs (provedores de dados tabulares) que apresentam os dados em modos de exibição tabulares. Consulte a documentação do provedor OLE DB para OLAP para obter informações mais detalhadas sobre a sintaxe específica e os comportamentos que têm o suporte do provedor.

## <a name="adox"></a>ADOX

O ADOX (Extensões do Microsoft ActiveX Data Objects para linguagem de definição de dados e segurança) é uma extensão do modelo de objetos e programação do ADO. O ADOX inclui objetos para criação e modificação de esquema, bem como para segurança. Por ser uma abordagem da manipulação de esquema baseada em objeto, é possível escrever código que funcionará em várias fontes de dados, independentemente das diferenças em suas sintaxes nativas.

O ADOX é uma biblioteca associada aos objetos básicos do ADO. Ele expõe objetos adicionais para criação, modificação e exclusão de objetos de esquema, como tabelas e procedimentos. Além disso, inclui objetos de segurança para manter os usuários e grupos e para conceder e revogar permissões nos objetos.

