---
title: Objetos no Outlook PIA
TOCTitle: Objects in the Outlook PIA
ms:assetid: 1be732a6-d6da-4fa0-beaa-accf35db12d6
ms:mtpsurl: https://msdn.microsoft.com/library/Bb609459(v=office.15)
ms:contentKeyID: 55119778
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 434be5dc9193beaf9723530c6d963ed0a96d8884
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407027"
---
# <a name="objects-in-the-outlook-pia"></a>Objetos no Outlook PIA

Enquanto estiver navegando no Outlook Primary Interop Assembly (PIA) em um pesquisador de objetos, você notará que muitas classes e interfaces têm nomes familiares, em referência à objetos no modelo de objeto do Outlook. Alguns objetos no modelo de objeto precisam ter um mapeamento individual nas interfaces no PIA. 

Por exemplo, o **AddressEntry** está mapeado para a interface [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) e o objeto **AddressList** é mapeado para a interface [AddressList](https://msdn.microsoft.com/library/bb623538\(v=office.15\))no PIA. 

No entanto, a maioria dos outros objetos têm um mapeamento de um para muitos no PIA. Este mapeamento de um para muitos é aplicado a todos os objetos adicionados a partir do Outlook 2007 e alguns objetos existentes antes do Microsoft Office Outlook 2007. Este tópico lista as interfaces, classes e delegados .NET que são mapeados para um objeto COM e descreve como acessar um objeto no PIA Outlook. Ele também descreve algumas exceções no Outlook PIA onde os objetos estão ocultos ou preteridos no modelo de objeto com base em COM.

## <a name="helper-objects"></a>Objetos de ajuda

Esta seção ilustra as típicas classes auxiliares de um objeto no Outlook PIA usando o objeto **FormRegion**como um exemplo. O objeto **FormRegion** foi adicionado ao modelo de objeto do Outlook 2007. Relacionados para o objeto**FormRegion** no PIA são representantes ilustrados na Figura 1, interfaces e classes.

**Figura 1. O objeto FormRegion representado no modelo de objeto do Outlook e no PIA Outlook**

![O objeto FormRegion representado no modelo de objeto do Outlook e no PIA Outlook](media/pia-outlook-object-model.gif)

Uma interface que você pode acessar com mais frequência é o **FormRegion** e os membros de método, propriedade e evento do objeto é a interface[FormRegion](https://msdn.microsoft.com/library/bb652633\(v=office.15\)). No entanto, você não deve considerar a interface **FormRegion** .NET como uma imagem espelhada exata do objeto **FormRegion** COM; se examinar o Pesquisador de Objetos no Visual Studio, você descobrirá que a interface **FormRegion** é herdada de outra interface, a interface [ \_FormRegion](https://msdn.microsoft.com/library/bb645761\(v=office.15\)). Na verdade, a interface**FormRegion** é apenas uma das seguintes interfaces e classes que resultam da criação do PIA Outlook baseiam-se a biblioteca COM.

Para criar o Outlook PIA, o Outlook usa o Importador de Bibliotecas de Tipos (TLBIMP) no .NET Framework para converter definições de tipos da biblioteca de tipos COM em definições equivalentes em um assembly de tempo de execução em linguagem comum. Na COM, o objeto **FormRegion** é realmente um coclass que consiste em duas interfaces a seguir, definindo as interfaces que o objeto**FormRegion** implementa:

- A interface principal ** \_FormRegion**

- A interface do evento [FormRegionEvents](https://msdn.microsoft.com/library/bb611940\(v=office.15\))

TLBIMP diretamente importa ** \_FormRegion** e **FormRegionEvents** da biblioteca.

Além de importar a interface principal e a interface do evento, o TLBIMP cria uma interface .NET com o mesmo nome de objeto COM e uma classe .NET que usa o nome do objeto e acrescentado de "Classe". No caso do objeto**FormRegion**, o TLBIMP cria o seguinte:

- A interface do .NET **FormRegion**

- A classe .NET [FormRegionClass](https://msdn.microsoft.com/library/bb624204\(v=office.15\))

A partir das interfaces .NET e classe .NET mencionadas neste tópico, você sempre pode usar a interface .NET que o TLBIMP cria para acessar um objeto. Por exemplo, para acessar um objeto **FormRegion** em VB, você sempre pode usar a interface **FormRegion**, como no exemplo a seguir:

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
Sub DemoFormRegion(ByVal Region As Outlook.FormRegion)
    Dim MyFormRegion As Outlook.FormRegion = Region
    ' Additional method code here
End Sub
```

<br/>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook; 
void DemoFormRegion(Outlook.FormRegion region) 
{
    Outlook.FormRegion myFormRegion = region; 
    // Additional method code here
}
```

Para informações sobre a finalidade da interface principal e da classe .NET que o TLBIMP importa e cria respectivamente, confira [métodos e propriedades no PIA Outlook](methods-and-properties-in-the-outlook-pia.md). Para informações sobre a finalidade de interfaces relacionadas a eventos, representantes e classes de sink helper, confira[eventos no PIA Outlook](events-in-the-outlook-pia.md).

## <a name="deprecated-objects"></a>Objetos preteridos

Objetos substituídos na biblioteca de tipos de objetos são expostos no PIA Outlook. Por exemplo, os objetos** \_DDocSiteControl** e ** \_DRecipientControl** estão ocultos na biblioteca de tipos, mas exibidos no PIA.

Outro exemplo de um objeto obsoletos é o objeto **MAPIFolder**. Iniciando no Outlook 2007,a **pasta** objeto substituiu o objeto **MAPIFolder** no modelo de objeto. Soluções existentes devem substituir as referências a **MAPIFolder** pela **pasta**, e todas as soluções de novas a partir do Outlook 2007 devem usar somente o objeto**pasta**. Para obter soluções não gerenciadas, pesquisador de objetos do Editor do Visual Basic não lista os objetos**MAPIFolder** nem como um objeto oculto. 

Para obter soluções gerenciadas, mesmo que o Outlook PIA exponha uma interface de [pasta](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) na qual você possa acessar o objeto **pasta** e seus membros, o Outlook PIA também expõe o [MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)) como uma interface que define os membros do **objeto** pasta.

## <a name="see-also"></a>Confira também

- [Relacionando o PIA Outlook com o modelo de objeto](relating-the-outlook-pia-with-the-object-model.md)


