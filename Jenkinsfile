
node {
stage ( ’ Checkout ’ ) {
checkout scm
}
stage ( ’ Build ’ ) {
docker . image ( ’ trion / ng−c l i ’ ) . inside {
sh ’ npm install ’
sh ’ ng build −−progress false −−prod −−aot ’
sh ’ tar −cvz fdist . tar . gz −−strip −components=1 d i s t ’
}
archive ’ dist . tar . gz ’
}
stage ( ’ Test ’ ) {
docker . imag-e ( ’ trion / ng−c l i −karma ’ ) . inside {
sh ’ ng test −−progress false −−watch false ’
}
}
} 
