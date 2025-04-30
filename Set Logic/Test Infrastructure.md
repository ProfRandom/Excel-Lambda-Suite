
aCount = 0 OR bCount = 0 // either list empty
	"VOID"
	
aCount = bCount // lists same length
	"COEQUAL"
	
bCount < aCount
	AND naCount < bCount
		"OVERLAP"
	AND naCount = bCount
		"EMBEDDED"
		
bCount > aCount
	"SUPERSET"

