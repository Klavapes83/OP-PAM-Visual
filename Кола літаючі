#include <iostream>
#include "graphics.h"
#pragma comment(lib,"graphics.lib")
using namespace std;

int main()
{
	initwindow(800, 500);

	double x, x1, y, y1, dx, dy, dx1, dy1;
	int r, r1;
	srand(time(0));

	r = rand() % (getmaxx() / 10) + 20;
	x = rand() % (getmaxx() - 3 * r) + r;
	y = rand() % (getmaxy() - 3 * r) + r;
	dx = double(rand() % 201 - 100) / 100;
	dy = double(rand() % 201 - 100) / 100;

	for (int t = 1; t > 0; t--) {
		r1 = rand() % (getmaxx() / 10) + 20;
		x1 = rand() % (getmaxx() - 3 * r1) + r1;
		y1 = rand() % (getmaxy() - 3 * r1) + r1;
		dx1 = double(rand() % 201 - 100) / 100;
		dy1 = double(rand() % 201 - 100) / 100;
		if ((x1 - x) * (x1 - x) + (y1 - y) * (y1 - y) <= (r + r1) * (r + r1))
			t++;
	}


	while (1) {
		setcolor(15);
		circle(x, y, r);
		circle(x1, y1, r1);

		delay(10);

		setcolor(0);
		circle(x1, y1, r1);
		circle(x, y, r);

		if (((x + r + dx) >= getmaxx() - 10) or ((x - r + dx) <= 0))
			dx *= -1;
		if (((y + r + dy) >= getmaxy() - 10) or ((y - r + dy) <= 0))
			dy *= -1;

		if (((x1 + dx1 + r1) >= getmaxx() - 10) or ((x1 + dx1 - r1) <= 0))
			dx1 *= -1;
		if (((y1 + dy1 + r1) >= getmaxy() - 10) or ((y1 + dy1 - r1) <= 0))
			dy1 *= -1;

		if ((x1 - x) * (x1 - x) + (y1 - y) * (y1 - y) <= (r + r1) * (r + r1)) {
			dx *= -1;
			dx1 *= -1;
			dy *= -1;
			dy1 *= -1;
		
		}
		x += dx;
		y += dy;
		x1 += dx1;
		y1 += dy1;
	}
	closegraph();
}
