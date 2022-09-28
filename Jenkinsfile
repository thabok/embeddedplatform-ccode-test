node {

    checkout scm
    
    docker.image('btces/ep').inside('--network=jdn') {
        
        btc.startup()
        btcProfileCreateC(codeModelPath: 'CodeModel.xml')
        btcVectorImport(importDir: 'testcases')
        btcRbtExecution(createReport: true)
        btcWrapUp()
        
    }
}