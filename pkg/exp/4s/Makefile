# Copyright 2009 The Go Authors.  All rights reserved.
# Use of this source code is governed by a BSD-style
# license that can be found in the LICENSE file.

all: 8.out 8.5s

4s.8: 4s.go data.go xs.go
	8g 4s.go data.go xs.go

5s.8: 5s.go 4s.go data.go xs.go
	8g 5s.go 4s.go data.go xs.go

8.out: 4s.8
	8l 4s.8

8.5s: 5s.8
	8l -o 8.5s 5s.8

clean:
	rm -f *.8 8.out
