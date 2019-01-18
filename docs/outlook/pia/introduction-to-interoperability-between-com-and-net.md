---
title: Introdução à interoperabilidade entre COM e .NET
TOCTitle: Introduction to interoperability between COM and .NET
ms:assetid: 6b2d099a-ec6f-4099-aaf6-e61003fe5a32
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb610378(v=office.15)
ms:contentKeyID: 55119776
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3b19135900974c3fa379aa9f4acb18ee98a2f8c5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709184"
---
# <a name="introduction-to-interoperability-between-com-and-net"></a>Introdução à interoperabilidade entre COM e .NET

O desenvolvimento de COM (Component Object Model) e .NET tem sistemas de tipo amplamente diferentes e mecanismos para gerenciamento de tempo de vida de objetos, criação e herança de interfaces. 

Por exemplo, um tipo **Variant** no COM é um tipo de dados **System.Object** no .NET Framework. Para criar um objeto, um cliente COM chama [CoCreateInstance](https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance), ao passo que um cliente gerenciado pode usar palavras-chave como "new" ou "New", que são integradas em uma linguagem de programação gerenciada. 

Embora COM não ofereça suporte à herança clássica e um cliente COM gerencie uma contagem de referências internas fornecida por [IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) para liberar uma coclasse, um cliente gerenciado depende do coletor de lixo de CLR (Common Language Runtime) fornecido pelo .NET Framework para liberar um objeto. 

Dadas essas diferenças entre o desenvolvimento de COM e .NET, desenvolver um cliente gerenciado em um modelo de objeto COM requer um mecanismo que resolva essas diferenças. O RCW (Runtime Callable Wrapper) é um mecanismo que promove a comunicação transparente entre COM e o modelo de programação gerenciado.

Este tópico fornece uma descrição de alto nível de como o RCW facilita a comunicação entre COM e o modelo de programação gerenciado. Observe que, embora este tópico use o Visual Studio para ilustrar o mecanismo RCW, você pode usar um assembly de interoperabilidade fora do Visual Studio para desenvolver um cliente gerenciado.

## <a name="facilitating-interoperability-the-interop-assembly-and-rcw"></a>Promover a interoperabilidade: assembly de interoperabilidade e RCW

### <a name="compile-time"></a>Tempo de compilação

Um assembly de interoperabilidade define interfaces gerenciadas que mapeiam para uma biblioteca de tipos baseada no COM e com as quais um cliente gerenciado pode interagir. Para usar um assembly de interoperabilidade no Visual Studio, primeiro adicione uma referência para o componente COM correspondente. O Visual Studio gerará automaticamente uma cópia local do assembly de interoperabilidade. O assembly de interoperabilidade contém um namespace, sob o qual há uma interface equivalente gerenciada de cada objeto COM no modelo de objeto COM. 

A Figura 1 ilustra um cliente gerenciado que deseja usar uma biblioteca de tipos COM que define a coclasse X. O cliente gerenciado chama X, que é a interface equivalente gerenciada para a coclasse X, conforme definido no assembly de interoperabilidade. No tempo de compilação, o projeto gerenciado é compilado com informações sobre a classe X do assembly de interoperabilidade.

**Figura 1. Um aplicativo gerenciado compilado com um assembly de interoperabilidade que interopera com uma biblioteca de tipos não gerenciada**

![Um aplicativo gerenciado compilado com um assembly de interoperabilidade que interopera com uma biblioteca de tipos não gerenciada](media/pia-unmanaged-type-library.gif)
  
Em geral, desde que você defina uma referência a uma biblioteca de tipos, o Visual Studio gera uma cópia de um assembly de interoperabilidade para essa biblioteca de tipos. Pode existir inúmeros assemblies de interoperabilidade para descrever o mesmo tipo COM. No entanto, uma biblioteca de tipos pode ter apenas um PIA (Assembly de Interoperabilidade Primário), que é o assembly de interoperabilidade publicado pela biblioteca de tipos. Ao contrário de outros assemblies de interoperabilidade, o PIA não é gerado sempre que você adiciona uma referência no Visual Studio. Em vez disso, você instala o PIA no cache de assembly global (GAC) apenas uma vez em um computador. Quando você adiciona uma referência à biblioteca de tipos, o Visual Studio carrega o PIA automaticamente.

Para programar uma solução gerenciada para o Outlook, você deve usar o PIA do Outlook. Para incorporar informações do PIA do Outlook em um suplemento gerenciado, primeiro você deve instalar o PIA do Outlook no GAC. Se você estiver usando o Visual Studio para criar o projeto gerenciado, depois de adicionar uma referência à biblioteca de tipos do Outlook, o Visual Studio carregará o PIA. No navegador de objetos, sob o namespace Microsoft.Office.Interop.Outlook, você pode ver interfaces gerenciadas com nomes correspondentes a objetos no modelo de objeto do Outlook. Por exemplo, a interface de Conta corresponde ao objeto **Conta** no modelo de objeto do Outlook. Ao compilar o projeto gerenciado, essas informações serão incorporadas no seu executável.

### <a name="run-time"></a>Tempo de execução

No tempo de execução, com as informações fornecidas por um assembly de interoperabilidade, o CLR do .NET Framework cria um RCW para cada coclasse com que o cliente gerenciado interage. Observe que o tempo de execução cria apenas um RCW para cada coclasse, independentemente de quantas interfaces o cliente obteve da coclasse. O RCW é um tipo de classe do .NET Framework que encapsula a coclasse COM. O RCW controla as instâncias da coclasse e lança referências a ela apenas quando o cliente já não precisa mais do RCW. Dessa forma, um cliente gerenciado não precisa gerenciar o tempo de vida de um objeto da forma que um cliente não gerenciado faria com COM.

A Figura 2 ilustra um RCW interceptando uma chamada de API de um cliente gerenciado no tempo de execução, e usando as informações do assembly de interoperabilidade, mapeando de forma transparente a chamada à API correspondente na coclasse COM. O processo a seguir descreve como isso acontece:

1.  O cliente gerenciado chama um método "A" da classe "X", conforme definido no assembly de interoperabilidade de uma biblioteca de tipos COM.

2.  Se ainda não existir um RCW para a classe "X", o tempo de execução do .NET Framework usa as informações do assembly de interoperabilidade e cria um RCW para a classe "X".

3.  O RCW intercepta a chamada para o método "A", converte os argumentos nos tipos COM correspondentes e invoca o método A da coclasse X conforme definido na biblioteca de tipos COM.

**Figura 2. Um RCW intercepta uma chamada de um arquivo executável gerenciado e mapeia a coclasse para uma biblioteca de tipos não gerenciada**

![Um RCW intercepta uma chamada de um arquivo executável gerenciado e mapeia a coclasse para uma biblioteca de tipos não gerenciada](media/pia-unmanaged-type-library-2.gif)
  

## <a name="see-also"></a>Confira também

- [Por que usar o PIA do Outlook](why-use-the-outlook-pia.md)
- [Instalar e referenciar o PIA do Outlook](installing-and-referencing-the-outlook-pia.md)

