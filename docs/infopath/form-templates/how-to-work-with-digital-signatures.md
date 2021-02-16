---
title: Trabalhar com assinaturas digitais
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- assinaturas digitais [infopath 2007],InfoPath 2007, assinaturas digitais
localization_priority: Normal
ms.assetid: fd13fb71-aecf-47bb-8a6b-db70bd90ceeb
description: O modelo de objeto do namespace Microsoft.Office.InfoPath fornece recursos para trabalhar com assinaturas digitais de forma programática.
ms.openlocfilehash: ea657f80f6e38a06a91e19c245eadc203c7c580c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425572"
---
# <a name="work-with-digital-signatures"></a>Trabalhar com assinaturas digitais

O modelo de objeto do namespace [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) fornece recursos para trabalhar com assinaturas digitais de forma programática. 
  
## <a name="digital-signature-features"></a>Recursos de assinatura digital

Os recursos de assinaturas digitais fornecidos pelo InfoPath permitem que você: 
  
- Habilitar assinaturas para o formulário inteiro ou para conjuntos específicos de dados no formulário que podem ser assinados separadamente.
    
- Especifique, para cada conjunto de dados que podem ser assinados, se uma única assinatura ou várias assinaturas são permitidas e qual será sua relação. Por exemplo, você pode especificar se elas são co-assinaturas paralelas ou se cada nova assinatura se contrasigna todas as assinaturas anteriores.
    
- Especifique uma mensagem a ser mostrada aos usuários do formulário enquanto eles assinam o formulário.
    
- Inserir e ver uma assinatura no documento. 
    
- Exibir informações de não repúdio verificáveis que foram adicionadas a cada assinatura para aumentar a segurança. Essas informações adicionais, que incluem uma exibição do formulário como foram apresentadas a cada signante, fazem parte da assinatura e não podem ser removidas sem invalidar a assinatura. A qualquer momento, você pode chamar esses dados clicando na assinatura no formulário para exibir a caixa de diálogo Verificar **Assinatura Digital.** 
    
- Aproveite um modelo de objeto para trabalhar com assinaturas digitais. Adicione informações personalizadas ao bloco de assinatura em formulários totalmente confiáveis por meio do modelo de objeto de assinatura digital. 
    
## <a name="overview-of-the-digital-signatures-object-model"></a>Visão geral do modelo de objeto de assinaturas digitais

### <a name="the-sign-event"></a>O evento Sign

O modelo de objeto para assinaturas digitais fornece o evento a seguir.
  
|**Nome**|**Descrição**|
|:-----|:-----|
|[Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) <br/> |Ocorre após um conjunto de dados ter sido selecionado para assinar.  <br/> Você pode usar esse evento para manipular os dados armazenados na assinatura digital. Por exemplo, você pode adicionar dados de um servidor de data/hora confiável ou adicionar uma contrasignatura da transação no lado do servidor. Você também pode usar esse evento para bloquear a assinatura se o usuário atual não for membro de um grupo específico.  <br/> |
   
### <a name="the-signeventargs-object"></a>O objeto SignEventArgs

Um manipulador de eventos para o [evento Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) pode trabalhar com o objeto de evento [SignEventArgs,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.aspx) que fornece as propriedades a seguir. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.SignedDataBlock.aspx) <br/> |Obtém o conjunto de dados que gerou o [evento Sign.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx)  <br/> |
|[SignatureWizard](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.SignatureWizard.aspx) <br/> |Obtém ou define se a caixa de **diálogo Assinaturas** Digitais deve ser exibida.  <br/> |
   
> [!NOTE]
> No modelo de objeto de código gerenciado [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) fornecido com o InfoPath 2003, o objeto de evento [SignEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEvent.aspx) para o evento [OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2.OnSign.aspx) fornece uma propriedade **XDocument** para acessar o objeto **XDocument** do formulário associado ao evento. Isso não é necessário com modelos de formulário criados com o InfoPath Forms Services ou o InfoPath usando o modelo de objeto  [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) porque os membros do modelo de objeto da classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) podem ser acessados em código de formulário usando a palavra-chave (C#) ou **Me** (Visual Basic). Por exemplo, para acessar a [propriedade Signed](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Signed.aspx) da [classe XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) para determinar se um formulário está assinado, você pode digitar um  `this.Signed` ou  `Me.Signed.`
  
### <a name="collections-and-objects"></a>Coleções e objetos

O modelo de objeto para assinaturas digitais fornece as coleções a seguir.
  
|**Nome**|**Descrição**|
|:-----|:-----|
|[SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) <br/> |A coleção dos objetos [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) no modelo de formulário conforme definido no tempo de design no modo de design do InfoPath.  <br/> A [coleção SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) implementa propriedades que podem ser usadas para acessar os [objetos SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) associados a um formulário. O [objeto SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) associado a um formulário pode ser acessado por meio da propriedade [SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SignedDataBlocks.aspx) da [classe XmlForm.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx)  <br/> |
|[SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) <br/> |Contém uma coleção de [objetos Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) para cada [objeto SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) no formulário.  <br/> A [classe SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) implementa propriedades e um método que pode ser usado para acessar os objetos [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) associados de um formulário e criar uma assinatura. O [objeto SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) associado a [um SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) é acessível usando a [propriedade Signatures.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Signatures.aspx)  <br/> Ao usar o [método CreateSignature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.CreateSignature.aspx) da classe [SignatureCollection,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) tenha em mente que a assinatura não será escrita até que o método [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) seja chamado no objeto [Signature.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) Esses métodos podem ser chamados somente a partir do manipulador de eventos **Sign** de um modelo de formulário totalmente confiável.  <br/> |
   
O modelo de objeto para assinaturas digitais fornece os seguintes objetos.
  
|**Nome**|**Descrição**|
|:-----|:-----|
|[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) <br/> |Representa um conjunto de dados signatáveis em um formulário. O [objeto SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) fornece várias propriedades e um método que pode ser usado para interagir programaticamente com um conjunto de dados signatáveis.  <br/> |
|[Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) <br/> |Representa uma assinatura digital que foi adicionada a um formulário ou conjunto de dados signatáveis em um formulário. O [objeto Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) implementa propriedades que podem ser usadas para recuperar informações sobre a assinatura digital e o método [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) para escrever o bloco de assinatura digital XML e calcular seu valor de hash criptográfico.  <br/> |
|[Certificado](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Certificate.aspx) <br/> |Representa o certificado digital X.509 que foi usado para criar a assinatura.  <br/> |
   
## <a name="working-with-digital-signatures-programmatically"></a>Trabalhar com assinaturas digitais programaticamente

O modelo de objeto do namespace [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) fornece membros para interagir com assinaturas digitais programaticamente. Em particular, formulários totalmente confiáveis podem adicionar informações personalizadas ao bloco de assinaturas antes que ele seja confirmado, de acordo com a linha do tempo a seguir: 
  
1. O usuário opta por adicionar uma assinatura digital a um formulário.
    
2. A **caixa de diálogo Assinaturas** Digitais é exibida, o usuário clica em **Adicionar** e seleciona os dados para assinar.
    
3. O evento [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) para os dados selecionados representados pelo objeto [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) é gerado, e o método [Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Sign.aspx) do objeto [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) e o [método CreateSignature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.CreateSignature.aspx) da coleção [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) são executados. 
    
4. Todas as ações personalizadas opcionais são executadas.
    
5. O [método Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) do objeto [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) é executado. 
    
6. A **caixa** de diálogo Assinar é exibida para digitar um nome (ou selecionar uma imagem de assinatura), selecionar um certificado para entrar e inserir comentários. 
    
7. Quando o botão Assinar é clicado, a assinatura é adicionada à coleção de assinaturas do formulário e as informações de não  repúdio são capturadas e salvas com a assinatura (que pode ser exibida posteriormente clicando em Exibir Formulário Assinado na caixa de diálogo Assinaturas Digitais e clicando em Ver as informações adicionais de assinatura que foram **coletadas).** 
    
O exemplo a seguir invoca o método [Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Sign.aspx) quando o usuário assina os dados selecionados e redige a assinatura com um valor de timestamp recuperado de um serviço de timestamp confiável. 
  
```cs
public void FormEvents_Sign(object sender, SignEventArgs e)
{
   // Add a new Signature object to the SignedDataBlockCollection.
   Signature thisSignature = 
      e.SignedDataBlock.Signatures.CreateSignature();
   // Write the XML digital signature block and compute hash
   // for signed data.
   thisSignature.Sign();
   // Countersign the signature with a trusted timestamp.
   // Get the XML node storing the signature block.
   XPathNavigator oNodeSig = thisSignature.SignatureBlockXmlNode;
   XPathNavigator oNodeSigValue = 
      oNodeSig.SelectSingleNode(
      ".//*[local-name(.)='signatureValue']");
   // Get timestamp from a trusted timestamp service (fictitious).
   MyTrustedTimeStampService s = new MyTrustedTimeStampService();
   string strVerifiedTimeStamp = s.AddTimeStamp(oNodeSigValue.Value);
   // Add the value returned from the timestamp service to the 
   // unsigned part of the signature block.
   XPathNavigator oNodeObj = 
      oNodeSig.SelectSingleNode(".//*[local-name(.)='Object']");
   XPathNavigator oNode = oNodeObj.Clone();
   oNode.SetValue(strVerifiedTimeStamp);
   oNodeObj.MoveToParent();
   oNodeObj.AppendChild(oNode);
   e.SignatureWizard = false;
}
```

```vb
Public Sub FormEvents_Sign(ByVal sender As Object, _
   ByVal e As SignEventArgs)
   ' Add a new Signature object to the SignedDataBlockCollection.
   Dim thisSignature As Signature = 
      e.SignedDataBlock.Signatures.CreateSignature
   ' Write the XML digital signature block and compute hash
   ' for signed data.
   thisSignature.Sign()
   ' Countersign the signature with a trusted timestamp.
   ' Get the XML node storing the signature block
   Dim oNodeSig As XPathNavigator  = _
      thisSignature.SignatureBlockXmlNode
   Dim oNodeSigValue As XPathNavigator  = _
      oNodeSig.SelectSingleNode(_
      ".//*[local-name(.)='signatureValue']")
   ' Get timestamp from a trusted timestamp service (fictitious).
   Dim s As MyTrustedTimeStampService = New MyTrustedTimeStampService()
   Dim strVerifiedTimeStamp As String  = _
      s.AddTimeStamp(oNodeSigValue.Value)
   ' Add the value returned from the timestamp service to the 
   ' unsigned part of the signature block.
   Dim oNodeObj As XPathNavigator  = 
      oNodeSig.SelectSingleNode(".//*[local-name(.)='Object']")
   Dim oNode As XPathNavigator  = oNodeObj.Clone()
   oNode.SetValue(strVerifiedTimeStamp)
   oNodeObj.MoveToParent()
   oNodeObj.AppendChild(oNode)
   e.SignatureWizard = False
```


